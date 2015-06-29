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
using established carriers, like [Stripe].

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
