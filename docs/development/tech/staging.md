### Staging

Staging (also known as development) is the environment where the
client can test the latest changes. Ideally, it is as similar to
production as possible. Setting up a staging server should be a
immediate priority as soon as the development phase starts.

Always keep in mind:

- **Keeping staging up-to-date aids communication with your client**. Bugs
  and issues can be found faster, and dealt with on a timely fashion.

- **Staging should always pass all tests!** Everything on staging is a
  *candidate* release of your project. Treat this environment seriously:
  as *few*  bugs as possible should make it here.

- To help automatically keep track of the previous point, we have
  continuous integration/deployment tools set up in place. Read up on
  the deployment phase for more advice.
