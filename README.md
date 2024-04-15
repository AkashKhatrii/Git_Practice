## This is my path to learning all about Git and Github!

### Basics about Git and Github:
1. `Local repository` - private working copy 
2. `Working Directoy and Staging Area` - intermediate area where commits can be formatted and reviewed before completing the commit
3. `push` - send a change to another repository (may require permission)
4. `pull` - grab a change from a repository


#### Commands
1. `clone` - bring a repository hosted somewhere like Github into a folder or your local machine
2. `add` - track your files and changes to Git
3. `commit` - save your files in git
4. `push` - upload your commits to a git repo, like Github
5. `pull` - download changes forma remote repo to your local repo
### Initially:
1. `git config --global user.name "Your Full Name"`
2. `git config --global user.email "your_email@example.com"`

### Steps:
1. Created a folder in my local machine
2. Initialized git with `git init`
3. Open github and created a new repo, copied its url
4. Ran `git remote add origin {url}` to set the remote repo as the newly created repo
5. Ran `git add .` to add all the untracked files to the staging area
6. `git commit` to commit changes to the local repo
7. `git push origin main` to push the local changes to the `main` branch of the `origin`

**Branch 1 was created after the above line**

### Branches

#### Branch 1:
> In this, I will create a new branch named `branch1` and commit all the content before the Branches heading and see for myself how it works.

1. `git branch branch1` to create a new branch
2. `git checkout branch1` to switch to that branch and make changes
3. Then inside **branch1**, I made some changes which won't be visible here!
4. Pushed changes to remote as `git push origin branch1`

**Branch 2 was created after the above line**

#### Branch 2:
> All the changes fro here onwards are done on branch2 and later merged with the main branch.
> Means, the content from the heading *Branch 2* is written and pushed to branch 2 and never written or pushed to main branch.

1. Hello, this is branch 2 changes
2. This is great stuff!
   
#### Steps:
1. Push changes to remote branch2
2. Checkout to main branch
3. Merge branch2 with main

### Again on Main
Until the above i.e. `line 3` of **Branch 2** -> **Steps:**, changes were made to branch 2 and merged.

Let's see how I merged the branch (**very Important**):
1. After pushing my branch2 changes to remote, I did `git checkout main` to go to the main branch.
2. Then I ran `git merge branch2` to merge my branch2 changes with main
3. Then I did `git push origin main` to push this changes (merge) to remote

#### few points to note:
1. It is not necessary to push the changes of a branch to remote and then merge, we can make changes to a branch in our local env and then merge with main too!
   

### About Merge Conflicts (via analogy)
1. Suppose, we create two branches `branch1` and `branch2` after commiting some changes to the `main` branch.
2. Now, say we make some changes to `index.html` on `branch1` and merge it with `main`.
3. Then, say, we have made changes to the `index.html` on `branch2` and try to merge it with `main`, then we will get merge conflict beacuse we have pushed `branch1`'s changes to `main` and those changes are not available to `branch2` and if this branch is merged with `main`, then it will override the changes made by `branch1`.

   