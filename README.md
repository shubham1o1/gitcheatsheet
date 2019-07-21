# Git Cheatsheet

## GIT:

* Version Control Sytem
* Distributed (Not Centralized)
* Who made what changes, when (co-ordination between developers)
* Revert back
* Local and remote repos

## Concepts: 

* Tracks code's history
* Takes snapshot of your files, each time you commit
* Each snapshot can be visited
* Stage before you commit

---

# Basic commands: 

```bash

git init # initializes local git repo
git add <file> # add file(s) to index
git status # check status of working tree
git commit # commit changes to index

```

## Remote Repos commands: 

```bash

git push # push to remote repo
git pull # pull latest from remote repo
git clone # clone repository into a new directory

```
---
# Workshop:

### Goto project folder and open git bash and vs code there

``` bash

touch index.html # create index.html
touch app.js

# initialize git
git init

#Adding name and email to git
git config --global user.name "Shubham Subedi"
git config --global user.email "abc@gmail.com"

#adding to local repo
git add index.html

#check staging are
git status

#removing from staging area
git rm --cached index.html

#variants
git add *.html # add all .html files to staging area
git add . # all files to SA

```
### Commiting:
``` bash
git commit
```
* Editor opens, # for comment, (not done in VIM, VS Code was default, different arrangement for VIM)
* Write something in editor's window as a comment
* Close the edit then git makes commit automatically

**Alternatively:**
``` bash
git commit -m "Changed index.html"
```
### gitignore:
**To ignore some files to be committed even on :**  ```git add . ```
```bash
touch .gitignore
touch log.txt
```
**Open gitignore and type :**
``` 
log.txt
/dir2
```
**Now log.txt and the folder dir2 will not be commited you can check with following commands:**

``` bash
git add . 
git status
```
### Branches

``` bash
git branch login #creates a branch named login
git checkout login #works on new branch now in editor and in bash
git commit -m "Branch modified"

git checkout master
git status #changes made to login is not visble from master
git merger login #merge master and branch login
```
---

## Remote Repositories:
* Sign-in to Github
* Create a new repo
* Copy ```git remote add origin '[link]' ``` and paste in bash. This adds remote repository
```bash 
git remote #lists all the remote repository
origin 

git push -u origin master
```
* sign in form appear, log in and reload the github page. Files will be added
* after this you can just follow simple steps:

``` bash
touch readme.md
git add .
git push # no need for -u, origin, and no need to log in again
```

### Cloning:
Click on *clone or download* dropdown in github and copy the link provided. 

In new folder open bash and type the following :

```bash 
git clone [paste the link provided]
```

### Pull : 

If someone else made the changes to your repo and you want to import the changed files, use pull 

In original folder type: 
```bash
 git pull
 already upto date # if no changes is found this message is recieved
```
