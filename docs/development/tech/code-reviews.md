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
