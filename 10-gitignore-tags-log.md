env
*.log
node_modules/
target/
*.tmp

Create:
touch .gitignore

Then:
git status

Git will ignore matching files.
Interview question
Why do we use .gitignore?
To prevent unnecessary or sensitive files from being tracked by Git.

Examples:
- passwords
- .env
- logs
- build artifacts
- dependency directories
14. Tags
Used for release versions.
git tag
git tag v1.0.0
git tag -a v1.0.0 -m "Release 1.0.0"
git show v1.0.0

Remote:
git push origin v1.0.0

or:
git push origin --tags

15. HEAD
Know this because interviewers may ask.

HEAD represents the commit/branch you are currently working from.
git log --oneline

You can see where HEAD points.

Common examples:
HEAD
HEAD~1
HEAD~2
HEAD^

Meaning:
HEAD
→ current commit

HEAD~1
→ previous commit

HEAD~2
→ two commits before HEAD

Important Git Troubleshooting Commands
Put these in your quick reference:
```git status
git log --oneline
git log --oneline --graph --all
git diff
git diff --staged
git show <commit>
git reflog```

Especially learn git reflog
git reflog

It records movements of HEAD.

This can sometimes help you recover a commit after operations such as reset.

That's a good advanced interview topic.
Git Reflog 
For example:
git reset --hard HEAD~1

You realize:
"Oh no! I needed that commit."

Check:
git reflog

Find the previous HEAD and potentially recover it:
git reset --hard <commit-id>