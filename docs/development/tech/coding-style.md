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
