delete all local branch except the current branch using:
```
# reference https://stackoverflow.com/questions/10610327/delete-all-local-git-branches
# Windows CMD
for /f "tokens=*" %f in ('git branch ^| find /v "*"') do git branch -D %f
```
