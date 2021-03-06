# Git Cheat Sheet!
#### **Author :** Arnab Basak 
#### **Contact :** [LinkedIn](www.linkedin.com/in/arnab-basak/)
---
<br>

# Content

- [Git: Configurations](#Git-Configurations)
- [Git: Starting a repository](#Git-Starting-a-repository)
- [Git: Staging files](#Git-Staging-files)
- [Git: Committing to a repository](#Git-Committing-to-a-repository)
- [Git: Pulling and pushing from and to repositories](#Git-Pulling-and-pushing-from-and-to-repositories)
- [Git: Branching](#Git-Branching )
- [Git: Stash](#Git-Stash)

<br>

# Git: Configurations

Git allows you to set a global and per-project username and email address. You can set or change your git identity using the ***git config*** command.
```
   $ git config --global user.name "FirstName LastName"
```

Git allows you to set a global and per-project username and email address. You can set or change your git identity using the ***git config*** command.
```
   $ git config --global user.email "user@user.com"
```

You can get very specific about what you want colored and how; but to turn on all the default terminal coloring, set color.ui to true.
```
   $ git config --global color.ui true
```

Run ***git config --list***, showing system, global, and (if inside a repository) local configs.
```
   $ git config --list
```

<br>

# Git: Starting a repository

The ***git init*** command creates a new Git repository.
```
   $ git init
```

The ***git status*** command displays the state of the working directory and the staging area.
```
   $ git status 
```

<br>

# Git: Staging files

The ***git add*** command adds a change in the working directory to the staging area.
```
   $ git add <file-name>
```

To add change in multiple files in the working directory to the staging area.
```   
   $ git add <file-name> <another-file-name> <yet-another-file-name> 
```

***git add .*** stages new files and modifications, without deletions
```
   $ git add .
``` 

To add the files or changes to the repository
``` 
   $ git add --all 
```

***git add -A*** stages all changes
```
   $ git add -A 
```

To clear the cache, you use the ***git rm*** command.
```
   $ git rm --cached <file-name>
```

***git reset*** is a powerful command that is used to undo local changes to the state of a Git repo. Git reset operates on "The Three Trees of Git".
```   
   $ git reset <file-name>
```

<br>

# Git: Committing to a repository

The ***git commit*** command captures a snapshot of the project's currently staged changes.
```
   $ git commit -m "enter your message"
``` 

When using ***git reset --soft HEAD*** you will remove the last commit from the current branch, but the file changes will stay in your working tree. Also the changes will stay on your index, so following with a git commit will create a commit with the exact same changes as the commit you "removed" before.
```   
   $ git reset --soft HEAD
```

The ***git commit --amend*** command is a convenient way to modify the most recent commit.
```
   $ git commit --amend -m <enter your message>
```  

<br>

# Git: Pulling and pushing from and to repositories

To add a new remote in the directory the repository is stored at.
```
   $ git remote add origin <link>
```

The ***git push*** command is used to upload local repository content to a remote repository.
```
   $ git push -u origin master
```

Used to target an existing repository and create a clone, or copy of the target repository.
 ```
   $ git clone <clone link>
```

The ***git pull*** command is used to fetch and download content from a remote repository
```
   $ git pull
```

<br>

# Git: Branching 

To show the list of Git branch:
```
   $ git branch 
```

To create a Git branch by defining a **branch name**:
```
   $ git branch <branch-name>
```

To switch between Git branchs:
```
   $ git checkout <branch-name>
```

To merge two Git branch:
```
   $ git merge <branch-name>
```

Create and switch to the branch:
```
   $ git checkout -b <branch-name>
```

To delete a Git branch in local:
```
   $ git checkout -d <branch-name>
```

To delete a Git branch **forcefully** in local:
```
   $ git checkout -D <branch-name>
```

To delete a Git branch in Remote:
```
   $ git checkout <branch-name>
   
   $ git push origin --delete <branch-name>
```

To prune / remove local caches:
```
   $ git fetch -p
```

To create a **Feature** *(sub-branch)* branch under a **Dev** *(parent-branch)* branch
```
   $ git checkout -b <feature-branch-name> <parent-branch-name>

   $ git commit -am "Your commit message"

   $ git checkout <parent-branch-name>
   $ git merge --no-ff <feature-branch-name>

   $ git push origin <parent-branch-name>
   $ git push origin <feature-branch-name>
```

<br>

# Git: Stash

The git stash command takes uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from working copy:
```
   $ git stash
```

The modifications stashed away by this command can be listed with git stash list:
```
   $ git stash list
```

***git stash apply*** leaves it in the stash list for possible later reuse:
```
   $ git stash apply
```

***git stash apply*** leaves it in the stash list for possible later reuse, and **stash label** is used to make them identified:
```
   $ git stash apply <stash-label>
```

***git stash save*** just save these changes in somewhere in local system:
``` 
   $ git stash save "This is the message"
```

***Diff*** command is used in **git** to track the difference between the changes made on a file:
```
   $ git diff
```