[return](versioncontrol)

:erase:

```sh

#First make an orphan copy of the existing branch. An orphan copy is a copy of a branch which already has all the added local repository of the latest files without any commits.

git checkout --orphan reporeset

#Then commit all the default added files, delete the old branch, renembe the new branch with the old branch's name then fore push it to your existing remote repository.

git commit -m message
git branch -D main
git branch -m main
git push -f origin main

#This will not keep your old commit history around.
