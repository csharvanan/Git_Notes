# Day03 - Git, GitHub Essential Basic

## Git, GitHub Notes

## Remote Repository

- Remote repository is hosted on servers.

- Popular platforms:

  - GitHub

  - GitLab

  - Bitbucket

<br>

## Clone vs Pull

### Clone

                git clone repository_url

**Used for:**

- First time downloading a repository.

### Pull

                git pull origin main

**Used for:**

- Getting latest updates.

<br>
 
## GitHub Collaboration

### Repository Setup

**Steps:**

1. **Create repository**  

   Example: 
    
    - Create a new repo in GitHub → *MyProject*

2. **Add team members**  

   Example: 
   
   - Invite teammates via **Settings → Collaborators**

3. **Configure branch rules**  

   Example: 
   
   - Protect `main` branch → require PR before merge

4. **Add CODEOWNERS file**  

   Example: 
   
   - Add `CODEOWNERS` file → in **.github** folder

## Pull Requests (PR)

- **Purpose**:
- Review code  
- Discuss changes  
- Approve before merging  

### Example Workflow

    Feature Branch → Pull Request → Code Review → Merge

**Example:**

1. Developer creates branch `feature-login` 

2. Pushes code → opens PR to `main`  

3. Team reviews & comments  

4. After approval → merge into `main`


<br>

## GitHub Authentication (SSH - Secure Shell)

### Generate SSH key:

                ssh-keygen -t ed25519 -C "<git_email_id>"

### Checking Agent pid

                eval "$(ssh-agent -s)"

### Add key to SSH agent:

                ssh-add ~/.ssh/id_ed25519

### Test connection:

                ssh -T git@github.com

#

<image src="assets/images/git_ssh_key_add.png">

# 

<image src="assets/images/git_add_ssh_key.png">

## Git Clone and push Using SSH key (SSH - Secure Shell)

### Clone using SSH:

                git clone git@github.com:user/repo.git

### push using SSH:

                git push origin main

<image src="assets/images/git_clone_using_ssh.png">

# 

<image src="assets/images/git_push_result.png">

#### Note:

- SSH key **id_25519** file in the **.ssh** folder

#### Use:

- No need to enter username/password every time.

#

# Webhooks

- **Definition**

    A webhook is simply a real-time notification sent from one app to another when an event happens

### Example

- When you push code to GitHub, a webhook instantly notifies Jenkins, which then triggers an automatic build.

<image src="assets/images/git_webhooks.png">

#

###             <p align=center> *** Thank you *** 

##  <p align=center>    Day03 Task Completed