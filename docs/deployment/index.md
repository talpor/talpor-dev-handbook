## The Deployment Phase

A deploy is when you push your local changes to either the
staging/development server or the production server. It doesn't just
happen just the once when everything is done, but it's an event that
happens regularly, specially when you are pushing changes from local
to staging. When you push to production you should take extra care
because you might be dealing with real data from your client.

As a rule of thumb, we generally use AWS for all our servers since it
provides the highest level of flexibility and scalability you might
possibly need.

### The Checklist

This checklist is a list of stuff to make sure you are doing (or not
and why) when setting up or deploying to a server.

- Make sure you disable password logins through SSH. **Enable public
  key authentication only**. Don't change SSH server port from 22 to
  anything else: **Security by obfuscation is not security.**

- Use **sudo** and use a good password for both your public key and
  your account.

- Setup your firewall. Generally you'll want to block everything
  except ports 22 (SSH), 80 (HTTP) and 443 (HTTPS).

- Setup NGINX as a reverse proxy to your application server.

- Production should always use a trusted HTTPS certificate. Make sure
  to get it and set it up.

- Redis is a sweet piece of software. It's so good and versatile that
  you can use it from a cache backend to a job queue backend. Figure
  out if you need it in your stack and set it up.

- Make sure we do not leak secrets. **Make sure that if an API key is
  accessible by untrusted agents then it is a public key**. Don't
  version control secrets. **Use environment variables to store secret
  keys.**

- **Setup automatic backups for production.** Backup both the
  database, and user generated content and store it **offsite.**

- Log everything. Read on Logging & Errors below.

- Automate your usual deploy process. We suggest using Fabric for
  this.

### Provisioning

We have a set of Salt states to help with provisioning servers with
secure defaults. Don't be afraid to ask for them. There's an ongoing
internal effort to move application servers into isolated containers
(e.g. using Docker). If that sounds interesting, don't be afraid to
ask about that either. Many of our tools, for example our CI pipeline,
is built around the assumption that you are using Docker, so it might
be a good idea to use Docker from the get go.

### Errors and Logging

As a general rule of thumb, log everything. Log errors and
notices. Use your stack standard way to do this, **don't just spill
print statements all over the place.** If you are doing something
critical, like handling payments, make sure you log the transaction
once on a log file and once on your database.

We internally use sentry for error logging and notification. Setup a
different DSN for each of your servers and respond to errors swiftly.
