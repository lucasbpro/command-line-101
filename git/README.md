### General Configuration (First setup on your computer)

To set up Git with your name and email:
```shell
$ git config --global user.name "<Your-Full-Name>"
$ git config --global user.email "<your-email-address>"	
```

To see the git config parameters currently set, run
```shell
$ git config --list
```

### Replicate an existing remote repository into a local folder

If the git repository already exists (in GitHub, for example), just run
```shell
$ git clone <repository_path.git>
```

### Initializing GIT in a local directory

In case you haven't cloned a git repository to a local folder, but instead you have an ordinary folder with your project, then run
```shell
$ git init
```
This will make the local directory be a git folder (you will see that a .git folder is created within the local folder). So far, this is not connected to a remote repository. 

### Connecting a local directory to a remote repository

At first, you will need to run:
```shell
$ git remote add origin <remote-repository_url.git>
$ git push -u origin master		
```` 

For the next pushes, just run
```shell
$ git push
```

If you want to remember your remote repository URL, run
```shell
$ git config --get remote.origin.url			
```

### Check the status of the repository (are there changes not commited?)

This will output a list of changed files which have not been commited
```shell
$ git status
```

### Commiting changes 

To move all changes (listed by _git status_) to the stagging area, run
```shell
$ git add .
```

If you want to move only a specific file to stagging area, the command is
```shell
$ git add <file_name>
```

Files in the stagging area will be commited when user runs _git commit_. In case you want to remove all files from staging area, run
```shell
$ git reset			
```
To commit changes, just run
```shell
$ git commit			
```
However, it is a better practice to include a commit message, as follows
```shell
$ git commit -m "Inser a message here"
```
If you want to label your last commit with a tag, you then need to run
``` shell
$ git tag -a <insert_your_tag_here> 
```
If you want to label an older commit (not the last one) with a tag, you then need to know the specific commit SHA and then run
``` shell
$ git tag -a <insert_your_tag_here> <commit_SHA>
```

### Pushing changes to remote repository

Once commited, the changes can be pushed (uploaded) to the remote repository by running 
```shell
$  git push
```

### Updating your local repository with changes from remote repository

Before commiting your changes to a remote repository, your local rep must be updated. This is performed via
```shell
$ git pull	
```

### Removing current changes 

To update local repository with remote files without removing files from staging area
```shell
$ git checkout			
```

### Recovering older commits

To return files to specific commit, you will need to know the commit SHA and run
```shell
$ git reset --soft <commit_SHA>			
```
To undo all commits between current state and the commit identified by <commit_SHA>, run
```shell
$ git reset --mixed <commit_SHA
```
This will keep the modifications in the files, although the commits will be undone. In case you want to undo the commits between current state and the commit identified by <commit_SHA> and also remove the performed modifications, run 
```shell
$ git reset -- hard <commit_SHA>
```

## Creating branches
To crate a branch, just run the following command. then the branch will be created from your current files in the repository. After that, changes in the files will only apply to the created branch
```shell
$ git branch <branch_name>
```
To delete a branch, just run
```shell
$ git branch -d <branch_name>
```
To switch to a specific branch, run
```shell
$ git checkout <branch_name>
```
To switch to a branch which does not exist, run the following command (the specified branch will be created)
```shell
$ git checkout -b <branch_name>	creates a branch and switches to it
```

###  Merging branches 
The following command will merge <other_branch> to the current branch
```shell
$ git merge --no-ff <other_branch> 		
```

### Showing older commits and diffs

To see all existing commits, run
```shell
$ git log   		
```
The git log command might be too much. If you want a summary of all existing commits, run
```shell
$ git log --oneline		
```
To see how many files were changed/added/removed in each commit, run
```shell
$ git log --stat		
```
To see the commits and their respective tags, run
```shell
$ git log --decorate		
```
If you want a full picture of existing commits and branches, run
```shell
$ git log --oneline --decorate --graph --all       draws a tree with the branches and commits
```

### Performing diffs 
To see the diff between local and remote repository
```shell
$ git diff			
```

### Advanced 

To make sure that Git output is colored and that it will display the original state in a merge conflict:
```shell
$ git config --global color.ui auto				
$ git config --global merge.conflictstyle diff3			
```



	
