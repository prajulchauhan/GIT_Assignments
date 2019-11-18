# Assignment Solution by Prajul Chauhan



## Create a folder *ninja* at the root level of your cloned code

   

      mkdir ninja



## Add a file *README.md* with content "Trying fast forward merge"




	touch README.md

	echo "Trying fast forward merge" >README.md


 
## Create a branch *ninja* and move to it


	

	git checkout -b ninja



## Run *git status* command



	[root@ip-172-31-3-252 gittest]# git status
	On branch ninja
	nothing to commit, working tree clean



## Commit your changes to *ninja* branch


	
	[root@ip-172-31-3-252 gittest]# git status
        On branch ninja
        nothing to commit, working tree clean	



## Merge *ninja* branch to *master* branch make sure that a new commit get's created



	
	   git checkout ninja
	   touch readme.md
	   echo "this is ninja prajul"> readme.md
	   git add readme.md
	   git commit -m "updated"
	   git checkout master
	   git push origin master



## Assuming you are in *master* branch, modify *README.md* with content *Changes in master branch*, commit the changes in *master* branch.



	   echo "Changes in master branch"> README.md
	   git add README.md
	   git commit -m "updated"
	   git push origin master```



## Switch to *ninja* branch, modify *README.md* with content *Changes in ninja branch*, commit the changes in *ninja* branch.




	   git checkout ninja
	   echo "Changes in ninja branch"> README.md
	   git add README.md
	   git commit -m "updated"



## Merge *master* branch to *ninja* branch in such a fashion that changes of *master* branch overrides changes in *ninja* branch

	   

	   git merge ninja

	   Updating cf22f94..d7d137e
	   Fast-forward
	   readme.md | 1 +
	   1 file changed, 1 insertion(+)
	   create mode 100644 readme.md




## Revert the above merge commit





	git log
	
	commit 685c1c895daab8578dae51a5700dc3b567790ca5
	Merge: 79ce94d 10821c9
	Author: prajul.chauhan <prajul.chauhan@mygurukulam.org>
	Date:   Wed Oct 16 12:21:17 2019 +0000

    	Merge branch 'ninja'


	git revert 79ce94d 10821c9 -m 1

	[root@ip-172-31-3-252 gitcommand]# git revert -m 1 79ce94d 10821c9
	error: a cherry-pick or revert is already in progress
	[root@ip-172-31-3-252 gitcommand]# git revert 79ce94d 10821c9 -m 1
	error: a cherry-pick or revert is already in progress
	hint: try "git cherry-pick (--continue | --quit | --abort)"
	fatal: revert failed
	[root@ip-172-31-3-252 gitcommand]# git cherry-pick --abort
	[root@ip-172-31-3-252 gitcommand]# git revert 79ce94d 10821c9 -m 1



	[master be47931] Revert "updates"
 	1 file changed, 3 insertions(+)
	[root@ip-172-31-3-252 gitcommand]#





## Merge *master* branch to *ninja* branch in such a fashion that changes of *ninja* branch overrides changes in *master* branch




	[root@ip-172-31-3-252 gitcommand]# git checkout ninja
	Switched to branch 'ninja'
	[root@ip-172-31-3-252 gitcommand]# git merge master
	Updating d7d137e..be47931
	Fast-forward
	gitcommand/README.md | 3 +++
	1 file changed, 3 insertions(+)
	[root@ip-172-31-3-252 gitcommand]#




## Revert the above merge commit





	git revert (SHA1 ID)





## Merge *master* branch to *ninja* branch in such a fashion that changes of both branches gets accumulated.




	[root@ip-172-31-3-252 gitcommand]# git merge master
	Already up to date.
	[root@ip-172-31-3-252 gitcommand]# git push origin master
	Enumerating objects: 10, done.
	Counting objects: 100% (10/10), done.
	Compressing objects: 100% (6/6), done.
	Writing objects: 100% (7/7), 860 bytes | 860.00 KiB/s, done.
	Total 7 (delta 0), reused 0 (delta 0)
	To gitlab.com:prajul.chauhan/gitcommand.git
	cf22f94..be47931  master -> master
