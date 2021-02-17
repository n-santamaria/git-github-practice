# Practicing GIT GITHUB basics


## GitHub:-

- Keep track of code history
- Takes 'snapshot' of your files
- You run a commit command to take a snapshot
- You can visiy any snapshot at a time
- You can stage the files before committing or taking snapshot
- Branches: concept where you want to write your own logic of code and don't want to commit unil it's finished. By default it's branch is on master.


## Practice directory:-

`/home/neville/Practice/github`


## Git Basic Commands:-

#### Local Repo:-

<table>
	<thead>
		<tr>
			<th>Command</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>`$ git init`</td>
			<td>Initialize the local git repository</td>
		</tr>
		<tr>
			<td>`$ git add <file>`</td>
			<td>Add the files to the staging area i.e. index</td>
		</tr>
		<tr>
			<td>`$ git rm --cached <file>`</td>
			<td>To remove the file from the staging area i.e. index</td>
		</tr>
		<tr>
			<td>`$ git status`</td>
			<td>To check the files in the staging area</td>
		</tr>
		<tr>
			<td>`$ git commit`</td>
			<td>Commit the files from the staging area i.e. index</td>
		</tr>
		<tr>
			<td>`$ git branch <branch_name>`</td>
			<td>Create a new branch</td>
		</tr>
		<tr>
			<td>`$ git checkout <branch_name>`</td>
			<td>Checkout to the branch</td>
		</tr>
		<tr>
			<td>`$ git merge <branch_name>`</td>
			<td>Merge two branches</td>
		</tr>
	</tbody>
</table>


#### Remote Repo:-
<table>
	<thead>
		<tr>
			<th>Command</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>`$ git push`</td>
			<td>to push the local commits to the remote repository</td>
		</tr>
		<tr>
			<td>`$ git pull`</td>
			<td>to pull the latest changes from the remote repository</td>
		</tr>
		<tr>
			<td>`$ git clone`</td>
			<td>to copy the entire code base into your local directory</td>
		</tr>
		<tr>
			<td>`$ git remote`</td>
			<td>to check the remote repository. By default it will be empty if the project is initialize with git locally</td>
		</tr>
		<tr>
			<td>`$ git remote add origin <git_repo_url>`</td>
			<td>to add/map remote repo to local repo</td>
		</tr>
	</tbody>
</table>


## To ignore files to commit to repository:-

- Create a .gitignore file
- Make an entry of the file name not to be committed into the .gitignore file


## Command to install Git:-

`$ sudo apt-get install git`


## Git configure your git name and email:-

<table>
	<thead>
		<tr>
			<td>Command</td>
			<td>Description</td>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>`git config --global user.name '<your_name>'`</td>
			<td>Set user's name</td>
		</tr>
		<tr>
			<td>`git config --global user.email '<your_email>'`</td>
			<td>Set email</td>
		</tr>
		<tr>
			<td>`git config -l`</td>
			<td>To list all git config file</td>
		</tr>
	</tbody>
</table>


## Git branches:-

- By default repository is having a master branch.
- You can create multiple branches and write code and then merge the branch later to master branch.
- Best practice is: Whenever you are having a different piece of module to work on, it's better to create a branch and work on the module. Later after committing you could merge the branch with master branch.
- Note: files created in master branch or any other branch apart from the existing branch you're working, may create conflict during the merge.


#### Example:-

- git branch login
- git checkout login
	- Do some work
	- git add .
	- git commit -m 'Login changes'
- git chekout master
- git merge -m 'Merging login'
- git push