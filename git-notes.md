

git branch branchName - creates new branch called branchName
git checkout branchName - switch to be on the branch called branchName

git checkout - b branchName - creates branch and switch to it

Note: use git checkout to set your working commands to be based on the branch you want.

Two ways of combining work... merge and rebase

git merge - Merging in Git creates a special commit that has two unique parents. A commit with two parents essentially means "I want to include all the work from this parent over here and this one over here, and the set of all their parents."

git rebase targetBranch - takes current commit/work and copies to another targetBranch as a new commit. Leaves the old commit as a dead-end copy.



git merge master - merges master into the current branch

gib rebase master - merges back to master so any unmerged branches of master would get it on pull

HEAD - HEAD is the symbolic name for the currently checked out commit

Moving around

git checkout 


Branch forcing
One of the most common ways I use relative refs is to move branches around. You can directly reassign a branch to a commit with the -f option. So something like:

git branch -f master HEAD~3 - forces master branch to be set at 3 parents above the current commit (HEAD)


Reversing changes in git - reset and revert

git reset HEAD~1 - sets back one commit, as if never ocurred

git revert HEAD - commits changes that will reverse the current commit back to its previous commit state, sets master to new commit. 

Q? git revert refers to HEAD always?


git cherry-pick <Commit1> <Commit2> ...

Picks specific commits BELOW current location (HEAD)

git rebase -i HEAD~4 - interactive UI for reordering and picking (or not-picking) commits below HEAD~4

git commit --amend - updates the current commit with a minor change

git tag v1 
git tag v0 HEAD^



git add fileName - adds this file into the current branch

git commit -m "Message" - commits to local repo

git status - shows branch, branch source and status, outstanding changes, untracked files

git push origin master - pushes up to origin the branch master
