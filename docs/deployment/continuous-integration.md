## Continuous Integration at talPor

This is an overview of how Continuous Integration (CI) is done at
talPor. All that is documented here is basically what we believe to be
the best approach for integrating your project into our internal CI
workflow. Read it, and make the changes you believe are needed for
your project.

### Technology choices

This is an opinionated document. While we don't force you to use any
of the stuff that is talked about in here, the tools we have developed
assume many of the practices we preach about here. Particularly, our
technology choices are based around the internal desire of simple
reproducibility and commitment to ship better software that scales
gracefully.

The only technology choice that cannot be avoided is **Jenkins** as it
is the selected CI workhorse. Besides that, all choices can be changed
as needed. However, in this document we assume the following:

1. **Docker from development to production**. Every possible
   environment has a relevant image. Every process is dockerized into
   a container. We recommend using our **docker registry** to store
   images and share them with your peers and between servers.

2. **Fabric** is used to encapsulate steps in the workflow and help
   keep things reproducible. **Helper tasks** are maintained by our
   developers.


### Version Controlling for Good CI

The general idea of a CI workflow is as follows:


`git push origin master -> Begin CI Pipeline -> If everything is OK
(i.e. all tests pass) -> Push new build`

At talPor, we follow Git Flow. As it is recommended, we have a
mainline which is what production is currently running, and a
development line which is where all development happens. Our mainline
branch is called `production` and our development branch is called
`development` (some projects call it staging). As can be expected,
production servers run on top of the `production` branch, and
development/staging servers run on top of the `development` branch.

Developers create feature branches on top of `development`. When a new
feature is ready, it is merged into `development`.  When a new push is
ready to be made to production, `development` is merged into it and
then pushed. A similar process happens when there is a hotfix that
needs to be applied.

We have extended Git Flow to follow a better suited CI flow. The
general idea of CI is that every change that makes it into
`development` and `production` should be as problem-free as
possible. As such, we have decided to make the invariant of the
`development` branch the following:

**At any given moment, `development` is a candidate release of the
  project.**

As such, `development` should be ready to be merged into *production*
and be as problem-free as possible. We define *problem-free* as **all
tests pass**. To avoid human error (merges when some test fails), when
using CI, `development` is handled by a machine (i.e. changes are
pushed by Jenkins), and **it is not allowed to manually push changes
into it**. To allow for development to happen, we have added a new
branch, `master`, in which development continues normally.

### Stacking Environments

If you are using Docker containers, we strongly suggest you
encapsulate your environments into different images for each
environment. Try to move common and repeated behavior into common
images, and extend those images.

- **Common.** The common steps in all your images. This is the root of
  your build tree. Common tasks to perform here are installing system
  dependencies and setting up global environment variables.

- **Local (extends Common).** The environment developers will use in
  their personal machines. Common tasks to perform here are installing
  developer tools and requirements for local.

- **Testing (extends Common).** The environment where tests are
  run. This environment is central to CI. Make sure running your tests
  is the entrypoint for this environment.

- **Production (extends Common).** The environment used by production
  servers.

- **Development (extends Production).** The environment used in
  staging or development servers. Should be as similar to production
  as possible.

Since keeping all your environment up-to-date can be a hassle, we have
an internal Docker registry where we store the latest images so they
can be pulled from as soon as a build is done.

### The Generic Pipeline

Our recommended CI pipeline for our software projects is described
below. The first step is triggered when a push with changes on
`master` is received.

1. **Build new Docker images, if necessary.** Checks into the new
   pushed files are performed to detect whether or not to trigger a
   build. **Only relevant environment should be rebuilt**. For
   example, if the Common needs to be rebuilt, every image needs to be
   rebuilt, but if the Production image needs to be rebuilt, only
   Production and Development needs rebuilding. If any image fails to
   be built, the pipeline is stopped, and developers notified.

2. **Run Tests.** Using your Testing environment, spin a new
   container, and wait for tests to run. If all tests pass, move to
   step 3. If any test fail, then notify developers a build has failed
   to build.

3. **Push changes.** Merge `master` into development (those changes
   don't break anything), and push all the rebuilt images to the
   registry.

4. **Deploy**. Deploy changes to all the environment you want. By
   default, we suggest automatically pushing into staging/development
   and manually pushing to production when wanted.

### Notifications & Broken Builds

Notifications happen any time that a build fails. **When a build
fails, the whole team should focus on making `master` to succesfully
build again**. Notifications are sent via email to developers and team
members, and Slack spam happens. **Don't ignore broken builds.**
