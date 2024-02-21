# Git

### Push new branch to a remote Git repo
1- Create a new, local Git branch in your repository:
```
git branch new-branch
```
or
```
git checkout -b new-branch
```
or
```
git switch -c new-branch
```
2- push `new-branch` to the remote repository:
```
git push --set-upstream origin new-branch
```
or
```
git push -u origin new-branch
```
### Delete a local & remote Git branch 
1- Switch to another branch before you delete requested branch

2- Delete local Git branch:
```
git branch --delete old-branch
```
or
```
git branch -d old-branch
```
3- delete remote Git branch:
```
git push origin --delete old-branch
```