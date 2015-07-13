## Tech Standards

### Source Control

From the get go, use version control. This is not negotiable. At
talPor we use [Git](https://git-scm.com/) exclusively. For open source code,
we publish at [GitHub](https://github.com/) and for everything else we use
internal Git repositories.

Always keep in mind:

- **Don't rewrite public story!** Bad stuff happens when you do that,
    kittens die. Just don't do it.

- Try to make your commits as atomic as possible. If you feel like you
  have many commits that don't quite work up to a feature (which you
  have not yet pushed), you can squash them with a rebase.

- Follow
  [Git Flow](http://nvie.com/posts/a-successful-git-branching-model). However,
  we keep master as develop, and production as master. Use feature and
  hotfix branches.

- Write good commit messages. Use a good headline and, if needed,
  follow it by further details about the commit.

- Cherish the existence of `cherry-pick` and `bisect`. Learn how and when
  to use `rebase` and `reset`.

### Technology Stack

Choosing the project technology stack is one of the most important and
lasting decisions of a project. It's almost cruel that such an
important decision has to be made so early in a project life when so
many unknowns remain. When selecting the project technology stack,
many factors have to be balanced:

1. Stable tools with strong ecosystems and communities.
2. Tools which helps us develop fast, and iterate quickly.
3. Tools that will make us happy.

Many times is easy to select the hip technology for a project that
actually requires something radically different, and boring. Selecting
the technology stack is a lasting decision that should be **agreed
upon** by the team members.

The following subsections list some of the common choices we have made
at talPor, and some of the things to look out for.

#### **Web apps**

We are primarily a [Python](https://www.python.org/) shop. We
generally use [Django](https://www.djangoproject.com/) for our
projects, although we have successfully used
[Flask](http://flask.pocoo.org/) for smaller projects.  Additionally,
we have dipped our toes in the [Node.js](https://nodejs.org/) and
[Rails](http://rubyonrails.org/) world with varying levels of success.

We prefer Python and Django on the backend because there are no
surprises. There is no magic, there are no strongly held opinions but
rather a set of conventions to follow.

On the frontend, we use plain Javascript. We generally work on top of
a framework. We have used [Angular](https://angular.io/),
[Backbone](http://backbonejs.org/), and
[React](http://facebook.github.io/react/) in the past. Styling is
generally done using a combination of [SASS](http://sass-lang.com/)
and [Compass](http://compass-style.org/).

Always keep in mind:

- Use starting skeletons for your projects. For Django we have found a
  lot of success using
  [Cookiecutter Django](https://github.com/pydanny/cookiecutter-django)
  and for Javascript we have enjoyed using
  [Yeoman Generators](http://yeoman.io/generators/).

- **Be pragmatic.** Choose the right tool for the job.

#### **Mobile apps**

Make the pragmatic choice. While the experience is always better on
native applications over hybrid applications, sometimes the choice has
to be made in the interest of development time and resources.

At talPor we have taken on projects that were built on top of
[Cordova](http://cordova.apache.org/) using
[Ionic Framework](http://ionicframework.com/) with great results.

Always keep in mind:

- Select with your current project in mind. If your project needs
  access to the latest iOS or Android features which have not landed
  yet on PhoneGap, maybe going native is the best choice.

- From a designer point-of-view, designing for Android and iOS are
  completely different stories. From screen size to the expected user
  experience, it's all different. Keep this in mind when you decide to
  go hybrid route.

#### **Databases**

We are strongly biased towards using
[Postgres](http://www.postgresql.org/) for every new project. There
are some up and coming NoSQL stores, like Mongo, but we deem them a
little too immature for production.

However, we love and use [Redis](http://redis.io/) as a K-V store,
generally for caching and the backend for job queues.

#### **Tooling**

Choose tools that help you during all the project stages. Your tools
should help you while you are developing by providing a good
development environment. Your tools should help you make the
transition from local to staging and production as painlessly as
possible.

We primarily use [Fabric](http://www.fabfile.org), on top of the
common system tools we already have available. We also enjoy using
[Docker](http://www.docker.com) to aid environment
reproducibility. Other great tools are [Grunt](http://gruntjs.com/)
and [Gulp](http://gulpjs.com/).

#### **Services**

There are several services that solve many common problems. Don't be
afraid to use them if they save considerable amount of development
time. For example, [Mandrill](https://mandrill.com/) solves the
problem of transactional email beautifully with almost no overhead in
integration with the existing codebase.

Always keep in mind:

- Consider using services that fix non mission critical parts of your
  project. Evaluate them, and use them if they shorten your
  development time.

### Style

Whatever your technology stack, write code as idiomatically as you
can. Dive into your technology stack code style, follow their style,
and avoid making one sided decisions. As a common rule of thumb, when
you want to do something non-idiomatic, you should be able to first
convince a teddy bear and then convince a team member.

If you need to define code style for your project (i.e. we inherited a
code base), document it and follow it religiously.

Over anything, **emphasize clean code and readability**. Use comments
to explain non obvious code paths. **Don't be clever**. Don't over
optimize for the 1% case, think of the 99% case. If the 1% case
becomes a reality, you will be thankful you didn't implement the
overly complicated, obfuscated option but the easy to follow and to
the point option.

Always keep in mind:

- Many languages have a style guide. For example, Python has
  [PEP-8](https://www.python.org/dev/peps/pep-0008/).

- Many frameworks also have a style guide. For example, Django has its
  [Coding Style guidelines](https://docs.djangoproject.com/en/1.7/internals/contributing/writing-code/coding-style/).

- There are many community-driven and company-driven efforts to define
  good style. We enjoy following AirBnB's
  [JavaScript Coding Style](https://github.com/airbnb/javascript/). Google
  also maintains a repository of style guides for their C++, Python,
  Angular projects, among others.

- When no obvious choice can be made regarding style, select a style
  guide by consensus, and follow it religiously.

- Use linters. Set them up to follow the agreed upon code style in
  your project. Add configuration files to your Git repositories if
  necessary.

### Code Reviews

Code reviews are what happens when another person looks at code you
want to commit or have already commited. The main reason to have code
reviews is aid **code maintainability and catch problems early**. In
small teams, it ensures that at least two pair of eyes are familiar
with every bit of the codebase.

At the moment, code reviews happen on a request basis. We follow a
*pre-commit*, or *pre-push* philosophy. When you want a code review,
you can either request it to one of your team members, or request it
to another coworker. Once your code is approved by your reviewers, you
can proceed to merge your code with `master`.

Always keep in mind:

- It's easier (and faster) to request a code review on small changes
  (less than 100 lines) than on a huge feature (over 1000
  lines). **Push early, and push often**. If you anticipate a big
  feature which you want to have code reviewed, start requesting code
  reviews as soon as possible and work on them incrementally.

- **Pre-review your code.** Everybody's time is valuable. Don't
  request code reviews on code that doesn't follow code conventions,
  lacks testing, or is sloppy. As a rule of thumb, ask yourself if you
  would accept your code if you were the reviewer.

- If you are reviewing code, handle requests promptly. If you don't
  understand something stop early and ask for clarifications (either a
  rewrite of that chunk, or better comment structure). **Don't reject
  code because you would have done it differently**. The main purpose
  of code reviews is to have **maintainable code**.

- If a reviewer and a reviewee can't agree over a point, bring a third
  party (another reviewer) to mediate.

### Testing

We strive for 100% testing coverage. Write tests religiously for your
code. Test both your backend and frontend, your logic, and common code
paths. Test for invalid inputs, and malicious inputs. **Try to break
your code**. It is a lot better if you break it locally, rather than
on production.

While we are not strongly opinionated on the approach you take (TDD?
BDD? Red-Green-Refactor?), your codebase should be tested
against. Prefer throughly tested libraries, frameworks and apps over
poorly tested ones.

Always keep in mind:

- Good testing means shipping working code. **Be religious about
  testing your codebase.**

- No testing or poor, sloppy testing will result in bad code
reviews. Respect your teammates time, write good tests.

- Testing is central to our continuous integration system. Lacking
  tests means that we won't be able to catch regressions or problems
  automatically.

### Provisioning and Reproducibility

Spend time figuring out how to make the different environments in your
project easily reproducible. Getting someone on-board on the project
should be relatively fast and easy. Adding a new server should also be
relatively painless. Keep clear documentation on how to install a
development environment and how to perform a staging and production
deploy.

Always keep in mind:

- Use your technology stack dependency managers. For example, if you
  are using python use [pip](https://pip.pypa.io/en/stable/).

- There are several up and coming projects that handle reproducible
  environments. At talPor, we have successfully used
  [Vagrant](https://www.vagrantup.com/) and
  [Docker](https://www.docker.com/) in the past.

- Try to make your local environment as close to staging as possible
  and staging as close to production as possible.

- Be pragmatic about the previous point. You don't need a load
  balancer to run your local setup.

- Read on the deployment phase for more advice.

### Staging

Staging (also known as development) is the environment where the
client can test the latest changes. Ideally, it is as similar to
production as possible. Setting up a staging server should be a
immediate priority as soon as the development phase starts.

Always keep in mind:

- **Keeping staging up-to-date aids communication with your
  client**. Bugs and issues can be found faster, and dealt with on a
  timely fashion.

- **Staging should always pass all tests!** Everything on staging is a
  *candidate* release of your project. Treat this environment seriously:
  as *few*  bugs as possible should make it here.

- To help automatically keep track of the previous point, we have
  continuous integration/deployment tools set up in place. Read up on
  the deployment phase for more advice.

### Hotfixes

There are several ways to hotfix problems that can happen in
`production`. If the problem is already fixed on `master`, the easiest
way is to backport the changes. This can be done cherry-picking the
commits that fixes the problem (you are making atomic commits, right?)

However, sometimes problems only happen or affect `production`, in
this case, you will need to track down the problem and prepare a
hotfix branch. When you are done fixing the problem, make sure you
merge against production.

Always keep in mind:

- When hotfixing a problem, your tests should pass afterwards.
- If new tests are needed, add them to your hotfix branch.
- Use `git cherry-pick -n` to review the changes you are
  cherry-picking before commiting them into your current branch.

### Security

Whatever your project or application is, take a minute to understand
that what you are building will eventually have to deal with malicious
input and carefully crafted exploits. **Expect the best, but prepare
for the worse.** Test for malicious inputs, understand common attack
vectors (XSS, CSRF, SQL Injections, man in the middle, ...) and
mitigate them. Make sure you are *always* testing users for the right
permissions when trying to do something.

Understand that data in production is extremely valuable, for you,
your client and your client's clients. **Make scheduled backups and
store them off-site.**

**Use SSL when dealing with sensitive information.** Avoid storing
credit cards, or other sensitive information, and if you do, read on
how to do it *securely*. If you are processing payments, consider
using established carriers, like [Stripe](https://stripe.com/).

Stay on top of CVEs and security releases related to your stack. This
includes system wide exploits related to your OS and libraries, and
making sure your framework is running on the latest security release.

Always keep in mind:

- **Security is a process, not a result.** Plan ahead, dip your toes
  on the attack vectors, learn to mitigate them.

- Frameworks like Django offer many built-in security provisions. Use
  them when possible.

- Follow sites which track security releases. Our internal
  communication system is generally updated when a new vulnerability
  or security release of common software in our stack is released.

- **Don't roll out your own authenticating system.** But if you manage
  to convince anyone that this is a good idea, please use strong,
  salted, one way ciphers to store user passwords.
