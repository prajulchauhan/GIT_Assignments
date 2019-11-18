# Assignment Solution by Prajul Chauhan


 

## Suppose you have two branches say branch A and branch B. Currently you are working in Branch B.




	[root@ip-172-31-3-252 gitcommand]# git branch a
	[root@ip-172-31-3-252 gitcommand]# git branch

					   a
				       	 * master
	

	[root@ip-172-31-3-252 gitcommand]# git branch b
	[root@ip-172-31-3-252 gitcommand]# git branch

					 
					   a
					   b
					 * master


	[root@ip-172-31-3-252 gitcommand]# git checkout b




## Create any file with any content in branch B and add it in staging area but dont commit it.


 



		[root@ip-172-31-3-252 gitcommand]# touch readme2.md
		
		[root@ip-172-31-3-252 gitcommand]# echo "assignment is almost done"> readme2.md
		
		[root@ip-172-31-3-252 gitcommand]# ls
		
		gitcommand  ninja  readme2.md  readme.md
		
		[root@ip-172-31-3-252 gitcommand]# git add readme2.md
		
		[root@ip-172-31-3-252 gitcommand]# git commit -m "practice"
		
		[b c322914] practice
		 1 file changed, 1 insertion(+)
		 create mode 100644 readme2.md
		
		[root@ip-172-31-3-252 gitcommand]# vim readme2.md
		
		[root@ip-172-31-3-252 gitcommand]# git add readme2.md





## Try to switch to Branch A. If its failing, then find a way out to switch to Branch A without commiting file in branch B.





		[root@ip-172-31-3-252 gitcommand]# git checkout a
		
		error: Your local changes to the following files would be overwritten by checkout:
		        readme2.md
		
		Please commit your changes or stash them before you switch branches.
		Aborting
		
		[root@ip-172-31-3-252 gitcommand]# git status
		
		On branch b
		Changes to be committed:
		  (use "git reset HEAD <file>..." to unstage)

		        modified:   readme2.md

		[root@ip-172-31-3-252 gitcommand]# git stash
		Saved working directory and index state WIP on b: c322914 practice






##Read about git reset (Soft, Mixed and Hard) command and implement it in your local git repository. And write your observations in each method (Soft, Mixed and Hard) Note: Dont copy paste from the internet. Write it in very simple language.




	git reset is used for undoing changes. It has three forms in which it can be implemented:

### soft

	uncommit changes, changes are left staged.

### mixed

	uncommit+unstage changes; changes are left in working tree

###hard

	uncommit+unstage+delete changes, nothing left




## Create a shell script which will take a number "n" as a input from user and script will revert the changes upto "n" no of commits. And if "n" is greater than no of commits in the branch in your git repository, then it should print "Invalid input (Input provided is greater than no of commits in the branch)" 




	#! /bin/bash
	read -p "enter the number of commit you want to revert:" num
	if [ $num > $(git log --oneline | wc -l) ]
	then
	echo "Invalid Number"
	else 
	i = $(git log --oneline | awk 'NR==$num {print=$1}')
	git revert $i
	done;
	else
	echo "Invalid input (Input provided is greater than no of commits in the branch)"
	fi




# Create a shell script which will take below inputs from user
  1. Remove untracked file (yes/No)
  2. Remove untracked directories (yes/No)
  and script will remove files or directories from git repo acc to the inputs given by the user.




	#!/bin/bash

	function UserInput(){

	read -p "Do you want clean the Untracked Files Enter (YES/NO)" inputfile

	filecheck

	read -p "Do you want clean the Untracked Directory Enter (YES/NO " inputDirectory

	directorycheck

	}

	function filecheck(){

	if

        [ $inputfile == "YES" ]

	then

        git clean -f

	else  [ $inputfile == "NO"]

	then

        echo "Not cleaning "

	do

        echo " Wrong Input "

	fi

}

	function directorycheck(){

	if

        [ $inputDirectory = "YES" ]

	then

        git clean -f -d

	else  [ $inputDirectory == "NO"]

	then

        echo "Not cleaning "

	do

        echo " Wrong Input "

	fi

	}


