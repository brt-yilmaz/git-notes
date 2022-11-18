## Git Notes

`git add .` add to all changes in directory

> make a decision that git commits haven to be written in present or past tense imperative

> Commits can be written in vim or you can change default text editor

`git log --oneLine` to see commits in one line

`git commit --amend`  to modify last commit 

> .gitignore must be defined // for directory use slash at the end of the path
 
`git commit -am "message"` to commit in a single line

`git switch -c <branchName>` to create and switch branch

> before switching branch must be committed Otherwise, a file or folder that is not in any branch comes with it.

`git branch -d` to delete you have to be out of the branch

`git branch -m <newBranchName>` you have to be in same branch

`git merge <branchName>` head must be in the branch which you want to continue with it 

`git diff` Compares staging area and working directory // a is the info that staging area last new about ,b is the working directory  
`git diff HEAD` list all changes in the working tree since your last commit  
`git diff --staged` list changes  between stagced and head // --cached is the same  
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

`git checkout <commit-hash>` detached head > this command is useful if you want to make new branch in older commit    
`git switch <branchName>` to reattached  
`git checkout HEAD~1` to see previous commit, that cause to detached head  
`git switch -` to go last step before detached head  
`git checkout HEAD <filename>` to undo all changes since last commit in working directory  
> `git checkout -- <filename>` short way
  
`git restore <filename>` to restore to the contents in the HEAD // NOT **undoable** // same as `git checkout HEAD <filename>`   
`git restore --source HEAD~1 <filename>` for specific destination  
`git restore --staged <filename>` to unstaged   

`git reset <commit-hash>` to cut the commit not changes // you can put these  commits to another branch //  
`git reset --hard <commit>` to go specific branch and delete unstaged changes// unstaged commits will be lost  
`git revert <commit>` creates a brand new commit which reverses the changes from a specific commit  

> Before git clone make sure your are not in a repo

`git remote -v` to see details of remote git
`git remote rename <old> <newName>`
`git remote remove <name>`
`
`git branch -r` to check remote branches  
`git branch <remoteBranchName>` to work with another remote branch, git can track automatically
`
`git fetch <remoteName>` to fetch (only get data to local repository not working directory) to all branches
`git checkout origin/master` to see last fetched data on brach
`git fetch <remoteName> <remoteBrachName>` to fetch specific branch 
`
> git pull = git fetch + git merge 
>> change current working directory
>>> not recommended if you have uncommitted work

`git pull <remoteName> <branchName>`  
`git pull` get automatically origin and current branch data 

`git remote add upstream <linkForkedRepo>` to fetch data from original repo

`git rebase master` to see commit ordered by name     
`git rebase --continue` to continue rebasing after solve the conflict  
`git rebase -i HEAD~8` to make changes for commits *all commits are new, commits hash change too*  
`reword` to rename commit ***content stays*** 
`pick` to keep commit ***content stays***  
`fixup`discard commit and meld into previous commit ***content stays***  
`drop`to delete commit ***content lost*** 

