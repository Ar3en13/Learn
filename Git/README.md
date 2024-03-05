# Git
### Basic Git Commands
- 1
![alt text](img/git_01.webp "Basic Git Commands 1")

- 2
![alt text](img/git_02.png?raw=true  "Basic Git Commands 2")

- 3
![alt text](img/git_03.png?raw=true  "Basic Git Commands 3")

- 4
![alt text](img/git_04.png?raw=true  "Basic Git Commands 4")

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
2- Push `new-branch` to the remote repository:
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
3- Delete remote Git branch:
```
git push origin --delete old-branch
```