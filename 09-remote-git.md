```git remote -v

git remote add origin <url>

git push origin main

git push -u origin main

git pull origin main

git fetch origin

git branch -r```

origin
origin is normally the default name given to the remote repository when you clone or add one.

Fetch vs Pull vs Push
Put this table in your repository:
Command	Direction	Purpose
clone	Remote → Local	Copy repository initially
fetch	Remote → Local	Download changes, don't integrate
pull	Remote → Local	Download + integrate
push	Local → Remote	Upload commits