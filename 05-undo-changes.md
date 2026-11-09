git reset 
Soft
git reset --soft HEAD~1

Commit removed, changes remain staged.
Commit ❌
Changes → STAGED

Mixed
git reset --mixed HEAD~1

Commit removed, changes remain unstaged.
Commit ❌
Changes → WORKING DIRECTORY

--mixed is the default.
Hard ⚠️
git reset --hard HEAD~1

Commit removed and local changes discarded.
Commit ❌
Changes ❌

Easy memory trick
soft  → staged
mixed → unstaged
hard  → deleted

git revert 
git revert <commit-id>

Unlike reset, it doesn't remove the old commit.

It creates a new commit that reverses it.
A → B → C → D
            ↑
         revert C

Important DevOps interview question
A bad commit has already been pushed to production. Reset or revert?

Answer:
"I would generally use git revert because it creates a new commit that reverses the bad change without rewriting shared Git history."