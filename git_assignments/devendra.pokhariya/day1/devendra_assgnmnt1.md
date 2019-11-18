# Assigment 1 (Git)
 
Assignments
 
Must Do
 
## Initialize a local git repository

 git init 
 
## Run git status command
```
git status
Output :=
On branch master
No commits yet
Create a file README.md
touch README.md
 ```
## Run git status command
```
git status
Output: =
On branch master
No commits yet
Untracked files:
          (use "git add <file>..." to include in what will be committed)
    README.md
 ```
 
## Add file README.md in your local repository
```
git add README.md 
git commit -m “Adding README.md file”
Add My first interaction with Git content in README.md
echo “My first interaction with Git” >> README.md
 ```

## Run git status command

```git status
Output:=
On branch master
Changes to be committed:
      (use "git rm --cached <file>..." to unstage)
    new file:   README.md
Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)
    modified:   README.md
 ```
 
## Update file README.md in your local repository
```git add README.md
git commit -m " Added to Local repository "
[master (root-commit) 006753f]  Added to Local repository
     1 file changed, 0 insertions(+), 0 deletions(-)
     create mode 10754 README.md
 
 ```
## Run git status command
``` git status
Output:
no changes added to commit (use "git add" and/or "git commit -a")
 
 ```
## Create files README1.md README2.md README3.md README4.md
```
touch README1.md README2.md README3.md README4.md
 ```
 
## Run git status command
``` 
git status
output:=
On branch master
Changes not staged for commit:
      (use "git add <file>..." to update what will be committed)
      (use "git checkout -- <file>..." to discard changes in working directory)
    Untracked files:
  (use "git add <file>..." to include in what will be committed)
 
    README1.md
    README2.md
    README3.md
    README4.md
 
no changes added to commit (use "git add" and/or "git commit -a")
 ```
## Add all the newly added files in your local repository without giving their name.
```
git add -A
git commit -m “new files added”
``` 
## Run git status command
```
git status
``` 
## Remove files README1.md README2.md from local repository
```
rm README1.md
rm README2.md
``` 
## Add content in Temporary content in README3.md
```
echo “temp content” >> README3.md 
Run git status command
git status
output:=
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)
 
    deleted:    README1.md
    deleted:    README2.md
 
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
 
    modified:   README3.md
 
``` 
## Find out the content that is added in README3.md
```
git diff README3.md
diff --git a/README3.md b/README3.md
index e69de29..de14eb1 100644
--- a/README3.md
+++ b/README3.md
@@ -0,0 +1 @@
+temp content
 
 ```
 
## Undo the changes in README3.md file
```
git reset README3.md
output:=
Unstaged changes after reset:
M    README3.md
 
``` 
## Run git status command
```
git status
Output:=
On branch master
Changes to be committed:
      (use "git reset HEAD <file>..." to unstage)
 
    deleted:    README1.md
    deleted:    README2.md
 Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)
 
    modified:   README3.md
 
 
``` 
## Create a branch ninja from current branch
```
git branch ninja
 
Create sensei branch from ninja branch and switch to sensei branch
 git checkout ninja
Switched to branch 'ninja'
git branch sensei
git checkout sensei
 
``` 
## List out all the local branches
```
git branch
  master
  ninja
* sensei
``` 
## Delete sensei branch
```
git checkout ninja
git branch -d sensei
Deleted branch sensei (was d83283e).
 
``` 
## Find out the current branch
```
git branch
  master
* ninja  (current branch )
 
``` 
## List out all the commits that have been done
```
git log
7f8 (HEAD -> ninja, master)
Author: devendra.pokhariya <devendra.pokhariya@mygurukulam.org>
Date:  Sun Oct 13 23:28:28 2019 -0700

Stagged all the data

commit b2e0b5da83b5863c9584e425a493824cd1ea6b64
Author: devendra.pokhariya <devendra.pokhariya@mygurukulam.org>
Date:   Mon Oct 14 14:22:27 2019 -0700
 
     4 files are added to local repository
 
commit 006753f87686e56441153d6cf34f30c06d5e4636
Author: devendra.pokhariya <devendra.pokhariya@mygurukulam.org>
Date:   Mon Oct 14 15:16:31 2019 -0700
 
     Added to Local repository
….
 
 
``` 
# Good To Do
 
## Create a shell script that will take a Git URL Number of days as input and it will list out all the commits that have been done in last n number of days. The script should display information like given below. A commit will be treated as valid one if it starts with a JIRA id [JIRA-xxxx]:
 
 
## Date/Time, Author Name, Author Email, Commit Message, Valid Commit Message
 
## Enable a functionality in your local repository to not allow a commit if it follows above condition of a valid commit message
 
 
# Learning
## In this section you learned all the basic commands of git to manage local repository
 
 
9:38 PM
Assignment 2 (Git) 30K Feet View
Introduction
In this section we will build understanding around git remote repo management
References
 
https://git-scm.com/docs
https://github.com/joshnh/Git-Commands
 
 
# Assignments
 
## Must Do
 
## Create a GitLab account if it doesn't exists already.

Done! Created -->
[] https://gitlab.com/devendra.pokhariya

Go to project → New project
 enter name GitCommand
Save


## Delete repo *GitCommand"

Go to project page
go to setting in left side bar
Advanced
Housekeeping, export, path, transfer, remove, archive.
Expand the setting and delete the repo

Fork https://github.com/joshnh/Git-Commands
 in your GitLab account with the name GitCommand
  Forked
https://github.com/devendrapokhariya/Git-Commands
https://github.com/devendrapokhariya/Git-Commands

## Clone GitCommand repo using http protocol
   ```
 git clone “https://github.com/devendrapokhariya/Git-Commands.git”
    git clone “https://github.com/devendrapokhariya/Git-Commands.git”
Cloning into 'Git-Commands'...
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 110 (delta 0), reused 0 (delta 0), pack-reused 109
Receiving objects: 100% (110/110), 18.55 KiB | 487.00 KiB/s, done.
Resolving deltas: 100% (31/31), done.
```
## Delete the cloned code
```
    rm -rf Git-Commands
 ```

## Create a folder ninja
   ```

    mkdir ninja
``` 
## Clone GitCommand repo using git protocol at ~/ninja
    
 ```
    cd ninja
git clone “https://github.com/joshnh/Git-Commands.git”
 
 ```
 
## Create a file README.md in ninja folder
 ```
touch README.md
```

## Make your changes available to GitCommand remote repo
```   
 git add .
    git commit -m “Adding README.md file”
    git push origin master
    Username for 'https://github.com': devendrapokhariya
Password for 'https://devendrapokhariya@github.com':
 ```
    
 
## Good To Do
 
## Get the latest code from remote repo without using git pull command
 ```
 git fetch
 ```
## Simulate above problem where instead of GitLab you would be using Git file server
 
## Simulate above problem where instead of GitLab you would be using custom Git SSH server
 
 
# Learning
## In this section you learned all the basic commands of git to manage local repository
```
init → It will initialize a bare repository in current directory.
add  → use to add files to index
status :- It will show all tracked and untracked file on your repository
commit :- Send your files to your staging area
rm :- it will delete files
diff :-  show difference of selected files
checkout :- used to switch between branches
branch :- to perform brancg operation Add, Delete ,
 ```
 


