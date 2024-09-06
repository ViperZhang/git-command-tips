## Download git
pls go to the offical website and install git
## Basic config
```
git config --global user.name 'enter your name'
git config --global user.name <enter your email address>
```
### example
```
git config --global user.name 'Zhuhua Zhang'
git config --global user.email zhuhuazhang@foxmail.com
```
## create a local repository
```
git init
```
## add files to index 
```
git add <filename>
git add . (all files in the current path)
```
## commit to local repository
```
git commit -m 'your commit (must have)'
```
### example
```
git commit -m 'Revise file1.txt and add xxx functions to this project......'
```
## other commands
```
git status 
git ls-files
git log 
git log --oneline
git reset --hard
git reset --soft
git reset --mixed
```
## about branch
### view local branch
```
git branch
```
### create local branch
```
git branch <branchname>
```
### switch branch
```
git switch <branchname>
```

## operate remote repository
```
git add remote <name (usuanlly use origin)> repo's SSH 
git remote rm <remote repo name>
git remote
git remote -v
git push -u origin master:main (从local的master分支推送到remote repo的main分支)
git clone <remote repo's SSH>[local path]
git pull <remote repo's name><remote repo's branch>
```