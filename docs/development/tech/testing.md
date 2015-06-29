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

- Good testing means shiping working code. **Be religious about
  testing your codebase.**

- No testing or poor, sloppy testing will result in bad code
reviews. Respect your teammates time, write good tests.

- Testing is central to our continuous integration system. Lacking
  tests means that we won't be able to catch regressions or problems
  automatically.
