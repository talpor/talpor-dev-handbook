### Provisioning and Reproducibility

Spend time figuring out how to make the different environments in your
project easily reproducible. Getting someone on-board on the project
should be relatively fast and easy. Adding a new server should also be
relatively painless. Keep clear documentation on how to install a
development environment and how to perform a staging and production
deploy.

Always keep in mind:

- Use your technology stack dependency managers. For example, if you
  are using python use [pip].

- There are several up and coming projects that handle reproducible
  environments. At talPor, we have successfully used [Vagrant] and
  [Docker] in the past.

- Try to make your local environment as close to staging as possible
  and staging as close to production as possible.

- Be pragmatic about the previous point. You don't need a load
  balancer to run your local setup.

- Read on the deployment phase for more advice.
