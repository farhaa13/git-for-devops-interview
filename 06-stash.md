```git stash
git stash list
git stash pop
git stash apply```

Named stash:
```git stash push -m "temporary changes"```

Delete:
```git stash drop```

Delete all:
```git stash clear```

pop vs apply
```git stash pop```
→ restore + remove stash

```git stash apply```
→ restore but keep stash

Interview scenario
"You have unfinished work but need to immediately switch branches."

Answer:
git stash
git switch another-branch