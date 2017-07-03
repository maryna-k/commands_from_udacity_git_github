# Cheat Sheet 
### List of commands used at course ["How to use Git and GitHub"](https://www.udacity.com/course/how-to-use-git-and-github--ud775) from Udacity


## Lesson 1

`diff -u <file1> <file2>`
compare two files,

`mkdir <dir_name>`
create a directory, 

`git log`
to get the list of commits,

`git diff <commit id1> <commit id2>` 
compare two commits. Useful if you want to find a specific bug or change,

`git log --stat`
gives statistics about which files have changes in each commit,

`git clone <URL>`
clone an existing repository,

`git clone <URL> <name of the directory>`
the same as the previous command except that you can specify the name of the directory,

`git checkout <commit id>`
to temporarily reverse history to this particular commit. Useful if there is a bug, but we are not sure in which commit it was introduced.


## Lesson 2

`ls -a`
to see hidden files,

`git init`
run this command in a directory that you want to transform into a repository. Ads .git file,

`git status`
check repository's status; shows the list of files changed since the last commit,

`git add <file> `
to add a commit to the staging area,

`git reset HEAD <file>`
to unstage,

`git commit` 
to commit and comment from the editor of choice,

`git commit -m "<comment>"`
to commit and comment from the command line,

`git diff`
this command with no arguments compares working directory to the staging area. It will show all the changes that are not staged. Usefull, if you don't remember your last changes that are not added to the staging area,

`git diff --staged`
compares staging are with the repository. Usefull if you want to double check the changes you are going to commit,

`git reset --hard` 
discards changes from the working directory of staging area,

`git branch <name>`
create a new branch,

`git checkout <branch>`
move to a specific branch,

`git log --graph --oneline <branch> <branch>`
shows graphic representation of 2 branches,

`git checkout -b <new_branch_name>`
from lesson "detached HEAD revisited". In case you made a commit that is not included in any branch, you might want to create a new branch. Otherwise, if you checkout an existing branch, this commit will be lost.

`git show <commit id>`
shows changes between specified commit and its parrent. Useful if the id of the parent commit is not known,

`git branch -d <branch name>`
deletes a specified branch. If this branch is not merged with another one, its commits will be unreachable after deletion and then lost!

#### To merge two branches:
1. `git checkout <branch1>`
2. `git merge <branch2> <branch1>` 
these two commands merge branch2 into branch1. It is important to checkout branch1 before merging.
3. If there are conflicts, open the file, resolve them and save the file.
4. `git add <file>`
5. `git commit`


## Lesson 3

`git remote`
shows current remotes,

`git remote add <name of the remote (origin)> <URL of the remote>`
adds remotes,

`git remote -v`
shows URL to fetch data from and to push data to,

`git push <remote to send changes to> <branch to push>`
sends changes to the remote,

`git pull <remote to pull from> <branch we want to pull from the remote>`
pulls changes from the remote (the local branch that pulled into should be checked out)

#### To fork a GitHub repository:
1. Fork a repository on GitHub website
2. `git clone <URL of your fork>` 
clone your fork to your local repository. When the repository is cloned, git automatically sets up a remote.

`git fetch <remote name>`
allows to update the master/origin branch without updating local master branch.
