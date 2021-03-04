# Let's use couple git commands with very short description
 Commands in execution order:
Right click inside desired local folder and choose: "Git Bash here"

1. git init // initialize git repository in the root of current folder where bash was initialized <br>
   git remote add origin	https://github.com/myusernameongithub/project-repository-url.git // atach server (called remote) to your local repository <br>
   git config --global user.email "youremail@email.com" <br>
   git config --global user.name "myusernameongithub" <br>
   git push origin main  // on first time access will ask for authorization on github <br>

   ssh-keyscan github.com >> ~/.ssh/known_hosts   // execute if error: The authenticity of host 'github.com (140.82.121.3)' can't be established <br>
   cd ~/.ssh && ssh-keygen                        // execute if error: git@github.com: Permission denied (publickey). <br>
                    will ask for a filename and a passphrase <br>

2. git add -A	// add files to repository 
3. git status	// check to see files that git detected as new, ready to be commited <br>
   git reset	// delete update before committing <br>
   git reset --hard origin/master  //  remove local changes or reset your local master to the state on remote <br>
   git diff master origin/master 	// see changes you'll be removing <br>
		&emsp; Navigating in view:  <br>
			&emsp;&emsp; Next line             : return  <br>
			&emsp;&emsp; Next page             : space bar <br>
			&emsp;&emsp; Previous page         : w <br>
			&#09;&emsp;&emsp; Quit viewing the diff : q <br>
			&emsp;&emsp; Help                  : h <br>
4. git commit -m "commit message" // create commit (-m with message)
5. git branch	//list branches and confirm existence of a branch
6. git checkout -b BranchVali // create a new branch (-b if branch does not exist)  <br>
   git checkout    BranchVali // switch to existing branch <br>
   git checkout main  // switch back to primary branch <br>
   git switch Existing-branch  // switch between branches <br>
   git switch -c Non-existing-branch // -c create branch if does not exist <br>
7. git push -u origin BranchVali     // push branch on github [(-u)remembers: location to push: "BranchVali" ]
8. // create pull request on web interface
9. // merge PR pull request
10. git pull origin main  // get changes on on github back to your computer  <br>
    git clone https://github.com/myusernameongithub/project-repository-link  // Copy entire repository (only once) to local machine (authorize asked if required)
11. git log  // see all commits
12. git branch -d LocalBranch // delete local branch (-d only if has been pushed and merged with remote branch)  <br>
    git branch -D LocalBranch // delete local branch (-D will force delete even if not pushed or merged)
13. git push origin --delete branch-to-be-deleted  //delete remote branch  <br>
    git push origin :branch-to-be-deleted  	   //delete remote branch - short version
15. git fetch -p  //  synchronize branch list (-p branches that do not exist on remote wil be deleted)
