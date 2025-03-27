# 30K Feet View

## Introduction
In this section we will build understanding around git advanced commands
* stash
* reset
* clean


## References
* https://www.atlassian.com/git/tutorials/resetting-checking-out-and-reverting

## Assignments
### Must Do
 
* Suppose you have two branches say branch A and branch B. Currently you are working in Branch B.
* Create any file with any content in branch B and then commit it. Alter the content again and add it in staging area but this time, dont commit it.
* Try to switch to Branch A. If its failing, then find a way out to switch to Branch A without commiting file in branch B.

* Read about git reset (Soft, Mixed and Hard) command and implement it in your local git repository. And write your observations in each method (Soft, Mixed and Hard) Note: Dont copy paste from the internet. Write it in very simple language.

* Create a shell script which will take a number "n" as a input from user and script will revert the changes upto "n" no of commits. And if "n" is greater than no of commits in the branch in your git repository, then it should print "Invalid input (Input provided is greater than no of commits in the branch)" 

* Create a shell script which will take below inputs from user
  1. Remove untracked file (yes/No)
  2. Remove untracked directories (yes/No)
  and script will remove files or directories from git repo acc to the inputs given by the user.



### Good To Do

* Change git log format to below format:
  <commit hash(red colour)> - <commit message(blue color)> - <commiter_date> 

* Read about Git Hooks.
  Using Git hooks vaildate the commit message. Eg: If any developer commits anything , then commit message should start from "Opstree--" string, otherwise it should print "Invalid commit message. Please start you ur commit msg with Opstree--" 

* Read about other advanced git commands.


## Learning

* stash
* reset
* clean
* revert
* Git Hooks
* Pretty Logs

