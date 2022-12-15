# git-learning-project
This project is for learning Git commands and Github workflow process
========================================================================================
GitIgnore file importance in git:

#                 --> Comments
Example: #Heading for First Project
/test.txt         --> ignore file which is in untracking phase at root level
/project/test.txt --> ignore file which is in untracking phase at specified level
 *.js             --> Ignore all files in the project with that extension
 build/           --> ignore the folder
 !main.js         --> donot ignore this file
========================================================================================
Git commit:
git commit verbose : git commit -v

========================================================================================
Git log command :
git log -p
# -p --> shows the changes for each commit
git log --oneline
git log --short
git log --oneline --all
git log --oneline --graph --all
git show <commitID>

========================================================================================
Git Remote Branching:

Git Branch commands:
git branch <branch-name> //create new branch
git checkout <branch-name> //switching of branches

git checkout -b <brnach-name> // create and switch to new branch

git fetch origin
git branch -a
remotes/origin/HEAD --> origin/main
remotes/origin/main

git merge origin/main

OR

git pull origin master
------------------------
My own assumption below:
In below text, Remote repository is always treated as origin,
It had a HEAD and default branch main (local and remote)
HEAD -->main, origin/main, origin/HEAD
(local)-->(local), (remote)/(remote), (remote)/(remote)

========================================================================================
Git Diff:
Git Merge:
Perforace tool installed on Mac. Need to configure
========================================================================================
Git Alias:
git config --global alias.alllogs "git log --oneline --graph --all"

========================================================================================
Git Stashing:
git stash push or git stash -- it will work on tracked files in stagged area only
git stash list
git stash apply //will take the last change and applies to our content but will not delete it from Stash
git stash apply stash@{1} //will take the last change and applies to our ""specific" content but will not delete it from Stash
git stash drop //this will remove the file that is available in stack and already restored
git stash pop // apply + drop
git stash -u //this will stash untracked files to stack
git stash branch oldidea
========================================================================================
Git Cleaning:
git clean -f  //forcefully
git clean -d //directory
git clean -x //permanently delete all untracked files in .gitignore
git clean -fdx //all above three operations
git clean -f --dry-run //dry run
========================================================================================
Git Rebase:

we have to be on master or main branch and run below command
git rebase <feature1-branch>
========================================================================================
Git Tagging:
git tag v1.0 //light weight tag
git tag -a v2.0 "This is second release"//annotated tag
git tag -l
git tag -l "v1.*"
git diff v1.0 v2.0 //difference or comparison between two tags
git tag -d v1.0 //delete a tag
git tag -a v1.0 <FirstcommitID> "Adding tag name for first time" //adding tag on a commitID
git tag -a v1.0 -f <SecondcommitID> // Updating the tag on different commitID
git push origin master v2.0 //push a particular tag
git push origin master --tags //pushes all tags
