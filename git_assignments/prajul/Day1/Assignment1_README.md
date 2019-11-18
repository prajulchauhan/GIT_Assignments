# Assignment Solution by Prajul Chauhan




## Initialize a local git repository 



	git init mylocalgit



## Run *git status* command



	gives state of working directory & staging area 



## Create a file *README.md* 



	touch README.md



## Run *git status* command 



	git status



## Add file *README.md* in your local repository



	 git add README.md



## Add *My first interaction with Git* content in *README.md*




	echo "My first interaction with git"> README.md





## Run *git status* command



 
	git status 




## Update file *README.md* in your local repository




	 git commit -m "message"




## Run *git status* command



	git status



## Create files *README1.md README2.md README3.md README4.md*



	touch README1.md README2.md README3.md README4.md




## Run *git status* command



		Untracked files:
			  (use "git add <file>..." to include in what will be committed)


			   nothing added to commit but untracked files present (use "git add" to track)



## Add all the newly added files in your local repository without giving their name.



	git add .



## Remove files *README1.md README2.md* from local repository

	

	rm -f README1.md

	
	rm -f README2.md




## Add content in *Temporary content* in *README3.md*



	echo "Temporary content" >> README3.md




## Run *git status* command



	On branch prajul
		Untracked files:
		  (use "git add <file>..." to include in what will be committed)

 		       ./

		nothing added to commit but untracked files present (use "git add" to track)




## Find out the content that is added in *README3.md*



	cat README3.md




## Run *git status* command



	On branch prajul
		Untracked files:
		  (use "git add <file>..." to include in what will be committed)

		        ./

			nothing added to commit but untracked files present (use "git add" to track)



## Create a branch *ninja* from current branch



	git checkout -b ninja




## Create *sensei* branch from *ninja* branch and switch to *sensei* branch

		


	git checkout -b sensei



## List out all the local branches



	  master
	  ninja
	  prajul
	* sensei



## Delete *sensei* branch

	

	git checkout ninja

	git branch -d sensei




## Find out the current branch



	  master
	* ninja
	  prajul



## List out all the commits that have been done



	Author: prajul.chauhan <prajul.chauhan@mygurukulam.org>
	Date:   Tue Oct 15 06:44:36 2019 +0000

	    adding readme3.md

	
	commit d00a1cbbc3158cb59ad7d5fe21a537e9776e00af
	Author: prajul.chauhan <prajul.chauhan@mygurukulam.org>
	Date:   Tue Oct 15 06:42:39 2019 +0000

	    adding readme.md

	
	commit 6fc3300d309d94ed2b1836cd35dc58674b9302a9 (origin/master, origin/HEAD, prajul, master)
	Author: Sandeep Rawat <sandeep@opstree.com>
	Date:   Tue Oct 15 11:23:56 2019 +0530

	    Defined commit format


