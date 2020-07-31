## GIT Setup

git config --global user.name "<Your-Full-Name>"		sets up Git with your name
git config --global user.email "<your-email-address>"		sets up Git with your email
git config --global color.ui auto				makes sure that Git output is colored
git config --global merge.conflictstyle diff3			displays the original state in a conflict
git config --list	

## Initializing GIT in a project folder

git init  			make folder a git folder
git clone			replicate a repository in a local folder
git status			shows the status of the folder (changes not committed?)

## PUSHING LOCAL FOLDER TO REMOTE REPOSITORY (GITHUB) FOR THE FIRST TIME

git remote add origin <remote-repository_url>		Faz o link do repositorio local com o remoto
git push -u origin master				Upload files for the first time

After that, you just need to type "git push" in order to upload files to remote repository.

git config --get remote.origin.url			To find out the remote rep url

## COMMITTING/UPLOADING FILES TO GIT REPOSITORY

git add <file> or . 		moves file (or all files - by using .) to the stagging area
git remote add origin <URL>     moves files to remote git repository
git reset			remove all files from staging area

git push						push changes up to remote repository
git push --set-upstream origin master 			initial push to set the remote as upstream
git push -u origin master				
git push origin <branch>				push changes up to branch named <branch>

git pull			update your local repository with changes in remote repository

git commit			comitt changes to repository with no message
git commit -m "<message>"	commit changes to repository with message

git tag -a v1.0			add tag to last commit
git tag -a v1.0	<commit_SHA>	add tag to specific commit of SHA=commit_SHA

## REMOVING CHANGES

git checkout			updates local repository with remote files, does not remove files from staging area
git checkout <branch>		switch to branch named <branch>
git reset			remove files from staging area
git reset --soft <commit_SHA>	returns version to specific commit		
git reset --mixed <commit_SHA>	undo other commits (after <commit_SHA>), but keeps modifications
git reset -- hard <commit_SHA>	undo other commits (after <commit_SHA>) and remove modifications from files	

##  MERGING BRANCHES
git merge --no-ff <other_branch> 		merge <other_branch> to current branch

## SHOWING COMMITS AND DIFFS 

git diff			show diff from local an remote repositories
git show    			for a specific commit
git log   			show existing commits
git log --oneline		summarizes the commits presenting only the commit messages for each of them
git log --stat			show how many files were changed and the number of lines that were added/removed
git log --decorate		show commits with tags
git log -p   			show existing commits with the modifications
git log --oneline --decorate --graph --all       draws a tree with the branches and commits


## CREATING BRANCHES 

git branch <branch_name>	creates a branch
git branch -d <branch_name>	delete a branch
git checkout <branch_name>	switches to a specific branch
git checkout -b <branch_name>	creates a branch and switches to it


	
