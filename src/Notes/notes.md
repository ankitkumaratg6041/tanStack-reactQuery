# Using Github for your project
### 1. Navigate to your project folder
cd /path/to/your/project-folder

### 2. Initialize a Git repository (if not already initialized)
git init

### 3. Add a GitHub repository as the remote origin
git remote add origin git@github.com:your-username/your-repository.git

### 4. Add and commit all files
git add .
git commit -m "Initial commit"

### 5. Push the files to GitHub
git branch -M main
git push -u origin main
---------------------------------------------------------------------------------------------------------

# Git Branches Notes
## 1. Creating a New Branch
A branch allows you to work on different features or fixes independently.
```
### Create a new branch
git branch branch-name

### Switch to the new branch
git checkout branch-name

### Create and switch to a branch in one step
git checkout -b branch-name
Example:

git branch feature/login
git checkout feature/login
OR


git checkout -b feature/login
```
## 2. Switching Between Branches
You can switch between branches to work on different parts of your project.

```
# Switch to an existing branch
git checkout branch-name
OR (Modern Git version):

# Switch to an existing branch

git switch branch-name

Example:
git checkout main
```

## 3. Viewing Branches
To check which branch you're on and view all available branches.

```
# List all branches
git branch

# List all branches with details (remote and local)
git branch -a

# Show the current branch
git status 
``` 

## 4. Pulling Changes from Another Branch
You can merge changes from one branch into your current branch by pulling.
```
### Switch to the branch where you want the changes
git checkout branch-name

### Pull changes from another branch into the current branch
git pull origin source-branch-name
Example:

git checkout feature/login
git pull origin main
```
**This merges changes from main into the feature/login branch.**

## 5. Merging One Branch into Another
Pulling from another branch internally performs a merge. If you want to merge manually:
```
### Switch to the branch where you want to merge changes
git checkout target-branch

### Merge another branch into the current branch
git merge source-branch
Example:
git checkout main
git merge feature/login
```
**This merges the changes from feature/login into main.**

## 6. Pushing Changes to a Branch
You can push changes from your local branch to the remote branch.
```
### Push the current branch to the remote repository
git push origin branch-name
Example:
### Push the feature branch to the remote repository
git push origin feature/login
```
## 7. Pulling from a Remote Branch
To get changes from a remote branch into your local branch.
```
### Pull changes from a specific remote branch
git pull origin branch-name

git pull origin feature/login
```
## 8. Deleting a Branch
Once you're done with a branch, you can delete it.

```
### Delete a branch locally
git branch -d branch-name

### Force delete a branch locally
git branch -D branch-name

### Delete a branch from the remote repository
git push origin --delete branch-name
Example:

### Delete a local branch
git branch -d feature/login

### Delete a remote branch
git push origin --delete feature/login
```

## Cheat Sheet

| **Command**                     | **Action**                                           |
|----------------------------------|-----------------------------------------------------|
| `git branch branch-name`         | Create a new branch                                 |
| `git checkout branch-name`       | Switch to a branch                                 |
| `git checkout -b branch-name`    | Create and switch to a branch                      |
| `git branch`                     | List all local branches                            |
| `git branch -a`                  | List all branches (local + remote)                |
| `git merge source-branch`        | Merge a branch into the current branch            |
| `git pull origin branch-name`    | Pull changes from a remote branch                 |
| `git push origin branch-name`    | Push changes to a remote branch                   |
| `git branch -d branch-name`      | Delete a branch locally                            |
| `git push origin --delete branch-name` | Delete a branch remotely                      |
