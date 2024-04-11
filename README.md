## This is my path to learning all about Git and Github!

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

### Branches

#### Branch 1:
> In this, I will create a new branch named `branch1` and commit all the content before the Branches heading and see for myself how it works.

1. `git branch branch1` to create a new branch
2. `git checkout branch1` to switch to that branch and make changes
3. Then inside **branch1**, I made some changes which won't be visible here!
4. Pushed changes to remote as `git push origin branch1`
