# Day01 - Git, GitHub Essential Basic

## Git, GitHub Notes

### **1. Version Control System (VCS)**

**What is Version Control System?**

A **VCS** is software that tracks and manages changes to source code or documents over time
- It lets multiple developers work on a project at the same time.
- It keeps a history of every modification so you can undo mistakes or return to an older version.
- Popular examples include Git, SVN, and Mercurial

### **Types of Version Control System** 

**(i) Local Version Control System** - Maintained in Local Computer

**(ii) Centerlized Version Control System (Subversion)**
- A central server story repository
- Developer pull code form server and make changer then push back to the server
- This **single point of failure** , If server goes down, development stops.

**(iii) Distributed Version Control Systerm (Git)**
- Every Developer has full copy of the repository including history (In Local Repository)
- **Not possible to single point of failure**

## Git Configuration (Register on Git with Username with Email)

                git config --global user.name "<git_username>"
                git config --global user.email "<git_email_ID>" 

## Git Architecture

## <p align=center>`Working Directory --> Staging Area --> Local Repository`

<image src="assets/images/Git_Architecture.jpg"></p>

## Flow of Git Working with commands

1. Intializing git on Repository (Creating **.git**) 

                git init .
    
    git --> metadata (Inforamtation about .git)
    
2. Creating file in ubuntu and Type the code (In Working Directory)

                touch <file_name>

3. Add  file into **Staging Area**

                git add <file_name>

    Adding Single to **Staging Area**

                git add .   

    Adding All file in that folder to **Staging Area**

## 

                git rm --cached <file_name>

Removing file form **Staging Area** that file back to **Working Directory**

                git status

displays the current state of your working directory and staging area.

##

4. Adding file into Local Repository

                git commit -m "<message to commit>

5. Checking Commited Status and ID

                git log
                git log --online    #showing commit satus in single line

#

# Working Examples
## Creating files and .git adding files to **Staging Area**
<image src="assets/images/git_add.png">

## Git commit and Status and Log Checking

<image src="assets/images/git_commit_status_log.png">

## Git add dot and commit, status and log checking 

<image src="assets/images/git_add_dot_commit_status_log.png">

#

# Commit and Tag

### **Commit:** 
A dynamic snapshot of your Project code changes identified by a unique hash, used to track daily development progress. (**SHA ID** Used)
### **Tag:** 
A static, human-readable label pointing to a specific commit, used to permanently mark major release milestones like `v1.0.0`.

The tag **`v1.0.0`** follows **Semantic Versioning (Major.Minor.Patch)** to track software updates:

* **`v1` (Major):**     --> Breaking changes (Version Update).
* **`0` (Minor):**      --> New features.
* **`0` (Patch):**      --> Bug fixes.

#

# Git Reset 

**`git reset`** is a powerful command used to undo changes, move the current branch head to a specific commit, and discard or stage modifications. (Remove Squential Commits for Mentioned Commit_ID to Top (latest) Commit_ID)

## Types of Git Reset

### **`--soft`**: 
Moves the branch pointer but keeps all your changed files staged in the Index. No work is lost.

### **`--hard`**: 

Destroys everything. It matches your tracking and working directory to the target commit, wiping away uncommitted changes.

## Examples

```bash

# Soft: Undo the last commit

            git reset --soft <commit_id>

# Hard: Completely wipe out the last commit

            git reset --hard <commit_id>

```
# 

# Adding more files to commit

## Creating file4, file5 the each file separately add to Staging Area and commit to Local repository.

<image src="assets/images/git_more_add_commit.png">

# Trying Soft and Hard Reset

## Soft Reset (If you reset with commit Id, It can restore if we want)

<image src="assets/images/git_reset_restore.png">

## Hard Reset (If you reset with commit Id, It cannot be restore if we want, it also delete the file in working directory)

<image src="assets/images/git_reset_hard.png">

# <h3 align=center> Day 1 Completed </h3>

# <h2 align=center>*** Thank You *** </h2>