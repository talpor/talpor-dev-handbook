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
