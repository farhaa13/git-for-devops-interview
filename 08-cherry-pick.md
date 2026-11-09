```git cherry-pick <commit-id>```

Meaning:
Apply one specific commit from another branch to the current branch.

Example:
feature branch:

A → B → C

main:

A → D

You want only C:
git switch main
git cherry-pick C

Now:
A → D → C'

Very useful scenario:
"A developer made a bug fix in another branch and you need only that fix in your branch."

Use:
git cherry-pick <commit-id>