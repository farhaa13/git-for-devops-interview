# Git for DevOps Interview Revision

Quick revision notes for fresher/junior DevOps Engineer interviews.

---

## 1. What is Git?

Git is a distributed version control system used to track changes
in source code, manage versions, create branches, collaborate,
and maintain code history.

## 2. Git vs GitHub

Git:
- Version control tool
- Runs locally
- Tracks code changes

GitHub:
- Remote Git repository hosting platform
- Collaboration
- Pull Requests
- Code Review
- CI/CD integration

---

## 3. Git Areas

Working Directory
        |
     git add
        ↓
Staging Area
        |
    git commit
        ↓
Local Repository
        |
     git push
        ↓
Remote Repository

---

## 4. Basic Commands

git init
git clone <url>
git status
git add .
git commit -m "message"
git push
git pull
git fetch
git log
git diff

---

## 5. Remote Commands

git remote -v
git remote add origin <url>
git push origin main
git pull origin main
git fetch origin

---

## 6. Branching

git branch
git branch <branch>
git switch <branch>
git switch -c <branch>
git merge <branch>
git branch -d <branch>

---

## 7. Merge Conflict

git status

Resolve the conflict manually.

git add <file>
git commit -m "Resolve merge conflict"

Abort:

git merge --abort

---

## 8. Stash

git stash
git stash list
git stash pop
git stash apply
git stash push -m "message"

pop  → restore + remove stash
apply → restore + keep stash

---

## 9. Reset

git reset --soft HEAD~1
→ commit removed, changes staged

git reset --mixed HEAD~1
→ commit removed, changes unstaged

git reset --hard HEAD~1
→ commit and local changes discarded

Memory:

soft  → staged
mixed → unstaged
hard  → deleted

---

## 10. Revert

git revert <commit-id>

Creates a new commit that reverses an earlier commit.

For shared/production branches, revert is generally safer
than rewriting history with reset.

---

## 11. Rebase

git rebase main

Replays commits on top of another branch.

Merge:
- Preserves history
- May create merge commit

Rebase:
- Cleaner linear history
- Rewrites history

---

## 12. Cherry-pick

git cherry-pick <commit-id>

Applies one specific commit from another branch.

---

## 13. Reflog

git reflog

Shows movements of HEAD and can help recover lost commits.

---

## 14. Tags

git tag
git tag v1.0.0
git tag -a v1.0.0 -m "Release 1.0.0"

Tags are commonly used for release versions.

---

## 15. .gitignore

Used to prevent unwanted/sensitive files from being tracked.

Examples:

.env
*.log
node_modules/
target/

---

## 16. Git + Jenkins

Developer
    ↓
Git push
    ↓
GitHub
    ↓
Webhook
    ↓
Jenkins
    ↓
Build
    ↓
Test
    ↓
Docker
    ↓
Deployment

---

## 17. Must-Know Interview Questions

1. What is Git?
2. Git vs GitHub?
3. clone vs fetch vs pull?
4. What is a branch?
5. What is a merge conflict?
6. How do you resolve a merge conflict?
7. reset vs revert?
8. soft vs mixed vs hard reset?
9. What is git stash?
10. pop vs apply?
11. What is rebase?
12. merge vs rebase?
13. What is cherry-pick?
14. What is reflog?
15. What is .gitignore?
16. How does Jenkins integrate with Git?
17. How can Git trigger Jenkins?