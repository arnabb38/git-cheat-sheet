# Git Cheat Sheet!


## Git: configurations
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


## Git: starting a repository
```
   $ git init
```
```
   $ git status 
```


## Git: staging files
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


## Git: committing to a repository
```
   $ git commit -m "Add three files"
```
```   
   $ git reset --soft HEAD^
```
```
   $ git commit --amend -m <enter your message>
```  