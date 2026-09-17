# Day02 - Git, GitHub Essential Basic

## Git, GitHub Notes

## Git Revert

Git revert is a safe way to undo changes by creating a new commit that reverses the effects of a previous (wanted) commit, without deleting history.

                git revert <commit_id>

### Working Example

<image src="assets/images/git_revert.png">

## Git Repository and Branching

- **Git repository** -> The complete project storage (all files + full commit history).

- **Branching** -> A way to create separate lines of development inside a repository.

**In short:** Repository is the container, branches are paths inside it.

### Git Branch Commands

- **Create new branch** 

            git branch branch-name  

- **Create + switch (one line)** 

            git checkout -b branch-name 

- **Switch branch** 

            git checkout branch-name 
            git switch target_branch_name

- **Delete branch** 

            git branch -d branch-name

- **List branches** 

            git branch 

### Worked Example

<image src="assets/images/git_branch.png">

## Git Braching Strategies

## 1. GitFlow

- **Structured workflow with multiple long-lived branches.**

- **Main branches:** 

  - `main`      → production-ready code
  - `develop`   → integration of features

- **Supporting branches:** 

  - `feature/*` → new features
  - `release/*` → prepare for release
  - `hotfix/*`  → urgent fixes

**Example:**

            git checkout -b feature-login

            git checkout develop

            git merge feature-login

## Trunk-Based Development

- Everyone commits to a single branch (`main` or `trunk`).

- Feature branches are **short-lived** (hours or <1 day).

- Continuous Integration (CI) ensures frequent testing and merging.

## Workflow
1. Create short-lived branch:
   ```bash
        git checkout -b feature-login
2. Work, commit quickly.

3. Merge back into trunk the same day:

            git checkout main
            git merge feature-login

#

# Git Merge vs Git Rebase

## 1. Git Merge
- **Definition:** 
    
    Combines changes from one branch into another while preserving history. (Entire Branch file merged to another branch)

- **Syntax**

            git checkout main
            git merge feature-branch

<image src="assets/images/git_merge.png">

## 2. Git Rebase
- **Definition:** 
    
    Re-applies commits from one branch on top of another, creating a linear history.

- **Syntax**

            git checkout feature-branch
            git rebase main

<image src="assets/images/git_rebase.png">

## 3. Git Squash

- **Definition:** 
    
    Combine Multiple commit into single commit.

    Clean commit history before squashing.

- **Syntax**

            git rebase -i HEAD~<no.of.last_sequential_commits>
            git rebase -i HEAD~3

<image src="assets/images/git_squash.png">

- After **git rebase -i HEAD~<no.of.squash>** Command its open nano Editor with Message.

    **Type Message --> Write Out (Ctrl + o) --> Press Enter --> Exit (Ctrl + x)**

#

# Git cherry-Pick

- **Definition:** 
    
    git cherry-pick is used to apply a specific commit from one branch into another branch without merging the entire branch history.

- **Syntax**

            git cherry-pick <commit-hash>

<image src="assets/images/git_cherry-pick.png">

# Git Merge Conflict

- **Definition:** 

    It happens when two people change the same part of a file differently (same line edited), 
    
    Git doesn’t know which version to keep.

<image src="assets/images/git_conflict.png">

- After this command **server.js** edited from master branch and added to Staging Area then it committed.

#

###             <p align=center> *** Thank you *** 

##  <p align=center>    Day02 Task Completed