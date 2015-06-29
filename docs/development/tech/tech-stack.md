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

#### Web apps

We are primarily a [Python] shop. We generally use [Django] for our
projects, although we have successfully used [Flask] for smaller
projects. Additionally, we have dipped our toes in the [Node.js] and
[Rails] world with varying levels of success.

We prefer Python and Django on the backend because there are no
surprises. There is no magic, there are no strongly held opinions but
rather a set of conventions to follow.

On the frontend, we use plain Javascript. We generally work on top of
a framework. We have used [Angular], [Backbone], and [React] in the
past. Styling is generally done using a combination of [SCSS] and
[Compass].

Always keep in mind:

- Use starting skeletons for your projects. For Django we have found a
  lot of success using
  [Cookicutter Django](https://github.com/pydanny/cookiecutter-django)
  and for Javascript we have enjoyed using
  [Yeoman Generators](http://yeoman.io/generators/).

- **Be pragmatic.** Choose the right tool for the job.

#### Mobile apps

Make the pragmatic choice. While the experience is always better on
native applications over hybrid applications, sometimes the choice has
to be made in the interest of development time and resources.

At talPor we have taken on projects that were built on top of
[PhoneGap](http://www.phonegap.com) and
[Cordova](http://cordova.apache.org/) with great results.

Always keep in mind:

- Select with your current project in mind. If your project needs
  access to the latest iOS or Android features which have not landed
  yet on PhoneGap, maybe going native is the best choice.

- From a designer point-of-view, designing for Android and iOS are
  completely different stories. From screen size to the expected user
  experience, it's all different. Keep this in mind when you decide to
  go hybrid route.

#### Databases

We are strongly biased towards using
[Postgres](http://www.postgresql.org/) for every new project. There
are some up and coming NoSQL stores, like Mongo, but we deem them a
little too immature for production.

However, we love and use [Redis](http://redis.io/) as a K-V store,
generally for caching and the backend for job queues.

#### Tooling

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

#### Services

There are several services that solve many common problems. Don't be
afraid to use them if they save considerable amount of development
time. For example, [Mandrill](https://mandrill.com/) solves the
problem of transactional email beautifully with almost no overhead in
integration with the existing codebase.

Always keep in mind:

- Consider using services that fix non mission critical parts of your
  project. Evaluate them, and use them if they shorten your
  development time.
