## Git Notes

`git add .` add to all changes in directory

> make a decision that git commits haven to be written in present or past tense imperative

> Commits can be written in vim or you can change default text editor for conflicts

`git log --oneline` to see commits in one line

`git commit --amend`  to modify last commit 

> .gitignore must be defined // for directory use slash at the end of the path
 
`git commit -a -m "message"` to commit in a single line

`git switch -c <branchname>` to create and switch branch

> before switching branch must be committed Otherwise, a file or folder that is not in any branch comes with it.

`git branch -d` to delete you have to be out of the branch

`git branch -m <newBranhcName>` you have to be in same branch

`git merge <branchname>` head must be in the branch which you want to continue with it 

`git diff` Compares staging area and working directory // a is the info that staging area last new about ,b is the working directory 
`git diff HEAD` list all changes in the working tree since your last commit
`git diff --staged` list changes  between staged and head // --cached is the same
`git diff HEAD <filename>` to see changes for only specific file
`git diff --staged <filename>`to see changes for only specific file
`git diff branch1 branch2` 
`git diff commit1 commit2`

`git stash` stash all uncommitted changes(staged or unstaged) 
`git stash pop` remove the stashed changes and re-apply them to your working copy
`git stash apply` stashed changes and re-apply them to your working copy 
`git stash list` to see multiple stash
`git stash apply stash@{2}` to apply specific stash
`git stash drop stash@{2}` to drop  specific stash
`git stash clear` to clear all stash 

git checkout <commit-hash> // detached head // git switch <branchname> to reattached
this command is useful if you want to make new branch in older commit
 
git checkout HEAD~1 // to see previous commit, that cause to detached head
git switch - // to go last step before detached head
git checkout HEAD <filename> // to undo all changes since last commit in working directory // git checkout -- <filename> short way

git restore <filename> // to restore to the contents in the HEAD // NOT undoable // same as git checkout HEAD <filename> 
git restore --source HEAD~1 <filename> // for specific destination
git restore --staged <filename> // to unstaged 

git reset <commit-hash> // to cut the commit not changes // you can put these  commits to another branch //
git reset --hard <commit> // to go specific branch and delete unstaged changes// unstaged commits will be lost
git revert <commit> // creates a brand new commit which reverses the changes from a spesific commit

before git clone make sure your are not in a repo
git remote -v // to see details of remote git
git remote rename <old> <newname>
git remote remove <name>

git branch -r // to check remote branches  
git branch <remoteBranchName> // to work with another remote branch, git can track automatically

git fetch <remoteName> // to fetch (only get data to local repository not working directory) to all braches
git checkout origin/master to see last fetched data on brach
git fetch <remoteName> <remoteBrachName> // to fetch specific branch 

git pull = git fetch + git merge // change current working directory // not recommended if you have uncommitted work
git pull <remoteName> <branchName>
git pull // get automaticly origin and current branch data 



