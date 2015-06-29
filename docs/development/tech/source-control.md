### Source Control

From the get go, use version control. This is not negotiable. At
talPor we use [Git] exclusively. For open source code, we publish at
[GitHub] and for everything else we use internal Git repositories.

Always keep in mind:

- **Don't rewrite public story!** Bad stuff happens when you do that,
    kittens die. Just don't do it.

- Try to make your commits as atomic as possible. If you feel like you
  have many commits that don't quite work up to a feature (which you
  have not yet pushed), you can squash them with a rebase.

- Follow [Git Flow](http://nvie.com/posts/a-successful-git-branching-model). However, we keep master as develop, and production as master. Use feature and hotfix branches.

- Write good commit messages. Use a good headline and, if needed,
  follow it by further details about the commit.

- Cherish the existence of `cherry-pick` and `bisect`. Learn how and when
  to use `rebase` and `reset`.
