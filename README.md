
### What is version control?
Version control is a way to track changes in a file, this file can be of any form(images, .exe, etc). The helps use to create  file history of the tracked files or snapshots of our files or source codes as the case may be while giving us the freedom to visit the snapshots(commits) of our files to revert back to a particular point in history(commit history).

### What is the difference between git and github?
Most folks are somewhat confused with the term git and github. Git is a version control software that allows us to track our files locally in our machine while giving us the advantage to move forward or backwards in our commit history as the need arises. 
Github is an online hosting platform that is used to host our local git tracked files on our various machines(personal computers) online and also facilitate collaboration, which is made possible when different individuals separated by geographical space can work on the same file simultaneously and remotely.

### What are the other github alternatives we have?
Other github  alternatives include: 
- Bitbucket
- Gitlab
- AWS Code Commit

### What is the difference between git fetch and git pull?
Git fetch simply downloads the recent changes from the branch you're currently on from the online repository without merging the changes. While git pull is simply a git fetch plus a merge. The recent changes are downloaded from the online repository of the current branch and merge to the branch of the local repository.

### What is  git rebase and the associated command?
Rebase in git simply means taking a commit and basing it off another commit. To put it in perspective let say we have a commit history of this sort

C1 -> C2 -> C3 -> C4
 Let say at commit C2 you created a new branch called feature(C5), let's call the feature branch commit C5. So to perform a rebase, i.e add C5 on top of C4. We do:
 
 We checkout to the feature branch using the below command:
 ```
 $ git checkout feature
 ```
 Thereafter we run this command:
 ```
$ git rebase main
 ```

 So now the commit history looks like this

C1 -> C2 -> C3 -> C4 -> C5'


### What is  git cherry-pick and the associated command?
The git cherry-pick command allows us to pick individual commits from any branch( using the commit hash ) and attaching it to our current branch.

It can be perform using the following commands.
```
$ git log --oneline --decorate
```
The above command produces the below output:
```
d1f9268 (HEAD -> feature, origin/feature) add interactivity to some icons and divs
f9e5e60 made changes to footer.
3f52db1 made changes the movie cards.
ddba576 made the movies.html responsive.
f556151 first commit
```
Inorder to move a particular commit, we take the commit hash  of the desired commit, which is a 7-digit truncated hash (by default it is a 40-digit hash) and run the below command in our terminal.

```
$ git cherry-pick f9e5e60
```
