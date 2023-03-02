
# return to [versioncontrol](versioncontrol)

:gitpush:

in order to push the local changes from your local repo to a
remote repo, you must [properly](localrepo) commit them
first and then you must [create](creategithubrepo) a remote
github repo_you must then configure your [ssh](sshgithub)
connetion to github_and then you must configure your local
repo's link, to that remote repo from github, by typing:

```sh

git remote add origin git@github.com:h4unted/haunt.git cat
.git/config

#and then type

git push origin main

```








git add remote origin main 
