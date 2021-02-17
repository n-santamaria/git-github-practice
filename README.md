# Practicing GIT GITHUB basics


## GitHub:-
-------------

- Keep track of code history
- Takes 'snapshot' of your files
- You run a commit command to take a snapshot
- You can visiy any snapshot at a time
- You can stage the files before committing or taking snapshot
- Branches: concept where you want to write your own logic of code and don't want to commit unil it's finished. By default it's branch is on master.


## Practice directory:-
-----------------------------
> /home/neville/Practice/github


## Git Basic Commands:-
----------------------------------

#### local repo:-
> $ git init 					: Initialize the local git repository
> $ git add <file>				: Add the files to the staging area i.e. index
> $ git rm --cached <file>		: To remove the file from the staging area i.e. index
> $ git status					: To check the files in the staging area
> $ git commit					: Commit the files from the staging area i.e. index
> $ git branch <branch_name>	: Create a new branch
> $ git checkout <branch_name>	: Checkout to the branch
> $ git merge <branch_name>		: Merge two branches


#### remote repo:-
> $ git push								: to push the local commits to the remote repository
> $ git pull								: to pull the latest changes from the remote repository
> $ git clone								: to copy the entire code base into your local directory
> $ git remote								: to check the remote repository. By default it will be empty if the project is initialize with 											  git locally
> $ git remote add origin <git_repo_url>	: to add/map remote repo to local repo


## To ignore files to commit to repository:-
------------------------------------------------------------
- Create a .gitignore file
- Make an entry of the file name not to be committed into the .gitignore file


## Command to install Git:-
-------------------------------------

> $ sudo apt-get install git


## Git configure your git name and email:-
--------------------------------------------------------------

> git config --global user.name '<your_name>'		: Set user's name
> git config --global user.email '<your_email>'	: Set email
> git config -l									: To list all git config file


## Git branches:-
--------------

- By default repository is having a master branch.
- You can create multiple branches and write code and then merge the branch later to master branch.
- Best practice is: Whenever you are having a different piece of module to work on, it's better to create a branch and work on the module. Later after committing you could merge the branch with master branch.
- Note: files created in master branch or any other branch apart from the existing branch you're working, may create conflict during the merge.

#### Example:-
------------

- git branch login
- git checkout login
	- Do some work
	- git add .
	- git commit -m 'Login changes'
- git chekout master
- git merge -m 'Merging login'
- git push