# Git Cheat Sheet!


## Git: Configurations

```
   $ git config --global user.name "FirstName LastName"
```
```
   $ git config --global user.email "user@user.com"
```
```
   $ git config --global color.ui true
```
```
   $ git config --list
```


## Git: Starting a repository

```
   $ git init
```
```
   $ git status 
```


## Git: Staging files

```
   $ git add <file-name>
```
```   
   $ git add <file-name> <another-file-name> <yet-another-file-name> 
```
```
   $ git add .
```  
``` 
   $ git add --all 
```
```
   $ git add -A 
```
```   
   $ git rm --cached <file-name>
```
```   
   $ git reset <file-name>
```


## Git: Committing to a repository

```
   $ git commit -m "enter your message"
```
```   
   $ git reset --soft HEAD^
```
```
   $ git commit --amend -m <enter your message>
```  


## Git: Pulling and pushing from and to repositories

```
   $ git remote add origin <link>
```
```
   $ git push -u origin master
```
```
   $ git clone <clone link>
```
```
   $ git pull
```


## Git: Branching 

```
   $ git branch 
```
```
   $ git branch <branch-name>
```
```
   $ git checkout <branch-name>
```
```
   $ git merge <branch-name>
```
```
   $ git checkout -b <branch-name>
```