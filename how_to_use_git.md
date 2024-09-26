## Download git
pls go to the official website and install git
## Basic config
```
git config --global user.name 'enter your name'
git config --global user.name <enter your email address>
```
If want to modify your name and email address in a specific project pls use commands as follows: remove --global 
```
git config user.name 'enter your name'
git config user.name <enter your email address>
```

### Example for add email and name
```
git config --global user.name 'Zhuhua Zhang'
git config --global user.email zhuhuazhang@foxmail.com
```
## Create a local repository
```
git init
```
If you have successfully created a local repo, you can input command: ls -la to see .git files
Note: .git files is a hidden files. If you use ls command you will not see it.
## Add files to index 
```
git add <filename>
git add . (all files in the current path)
```
## Check files in index
```
git ls-files
```
## Remove files from index
```
git rm --cached <file name>
```
## Add .gitignore file
```
touch .gitignore 
```
## Add file type in ignore file
```
vi .gitignore 
```
## Commit to local repository
```
git commit -m 'your commit (must have)'
git commit (Will go into a vim editor)
```
### Example
```
git commit -m 'Revise file1.txt and add xxx functions to this project......'
```
## Check files in workspace 
```
git status 
```
## Check commit log
```
git log 
git log --oneline
```
## Version reset (very important!!!)
```
git reset --hard
git reset --soft
git reset --mixed
```
## Branch process
### view local branch
```
git branch
```
### rename branch's name
```
git branch -m <new branch name>
git branch -M <new branch name> This command will force rename branch

```
### create local branch
```
git branch <branc hname>
```
### switch branch
```
git switch <branch name>
git switch -c <branch name>  create a new branch and switch to it
```
## Operate remote repository
### add link between local repository to remote repository
```
git add remote <name (usually use origin)> <remote repo's SSH>
```
### delete a remote repo
``` 
git remote rm <remote repo name>
```
### check which remote repo you have linked
```
git remote (only show the remote repo name like: origin)
git remote -v (can show the whole URL and two commands fetch and push)
```
### push files to remote repo
```
git push -u origin master:main (form local's master branch push to remote repo's main branch)
```
If you have rename you local repo's master branch as main (In Windows OS git default branch's name is master)
```
git branch -M main
```
you can input this command
```
git push -u <remote repo's name usually is original> main
```
One local repo can link two or more remote repos. Here are some useful commands
```
git remote add Github_repo github's SSH
git remote add Gitee_repo gitee's SSH
```
### clone a open source remote repo from github or gitee
```
git clone <remote repo's SSH> [local path]
```
Note: If you clone a remote repo to your local PC, the remote repo will automatically linked to your local repo (that you have clone from github or gitee)
### get the update files from repo
```
git pull <remote repo's name> <remote repo's branch>
```