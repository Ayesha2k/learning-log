# 🧠 Git Basics

This file contains notes and practice commands from my Git Basics learning.

## 1. 📚 freeCodeCamp – Git for Beginners

## 🎯 Learning Goals
- Why git and github are important?
- How to use them?
- Covering basic terms and commands.
- Understanding concepts like (repository, branching, merging, forking).
  
---

## 🪄 Core Concepts 
- Git is a **FREE** and **OPEN SOURCE** version control system.
- Version Control is a way for programmers to **TRACK CODE CHANGES**. Initial version of the document/code is saved on Git and every time the information is updated, it is saved on git. This helps in tracking bugs or rollback to a previous version of the document.
  
- **Git** vs **Github**<br>
  Git: Tool for tracking changes in your code overtime.<br>
  Github: Website to host your Git repositories, so that you can work online in teams an organise your projects in a portfolio.

- **HTTPS Vs. SSH**
   - To push changes from your local machine to Github account you have to prove that you are the owner of your account. This is done using **SSH Keys**.
   - Generate a key locally **ssh-keygen -t rsa -b 4096 -C"ayeshashah0208@gmail.com"**
   - View keys using **ls ~/.ssh**. Keys with extention **.pub** are public keys that has to be uploaded on your github.
   - Now each time you need to connect your local machine to Github, you will have the private key to show github that you create the public key.
   - Copy the public key using **cat ~/.ssh/id_rsa.pub** and paste on GitHub to add SSH key.
   - Add SSH Key to ssh-agent using below
       1. eval "$(ssh-agent -s)"
       2. ssh-add ~/.ssh/id_rsa
       3. ssh -T git@github.com
  
| Feature                  | HTTPS                                     | SSH                                          |
|--------------------------|-------------------------------------------|----------------------------------------------|
| URL Format               | `https://github.com/user/repo.git`        | `git@github.com:user/repo.git`               |
| Authentication Method    | GitHub username + Personal Access Token   | SSH key pair (public + private)              |
| Setup Difficulty         | Easy                                      | Moderate (generate and add SSH key to GitHub)|
| Prompts for Credentials  | Yes (unless cached)                       | No (once set up)                             |
| Security Level           | High                                      | Very High                                    |
| Use Case                 | Beginners, occasional users               | Professionals, automation, frequent users    |
| Recommended For          | Quick setup, temporary work               | Long-term use, industry standard             |

- **WORKFLOW**
  Adding code in github interface **Vs** Local git workflow
1. Adding code in github interface
   - No need for `add` --> github handles add and commit at the same time.
   - No need for `push` --> code is already live on github
   - If we dont own the repository/ dont have access rights and wanted to merge our code with rest of the code, then **pull** request is made.
     
   write code --> COMMIT changes -> PULL request
   
2. Local git workflow

   write code --> STAGE changes(git add) --> COMMIT changes(git commit) --> PUSH changes(git push) --> PULL request

- **Git Branching**
  - Master branch is the main/ default branch where all the code lives.
  - looks more like a TREE with multiple branches
  - Can create multiple branches for different purpose
    e.g. feature branch --> to add a new feature
         Hot fix branch --> to fix a bug
  - Changes made in a branch will only be visible to that branch, so changes(features, bugs etc.) can be made and committed(saved).
  - Branching is useful when multiple people are working on the same repository.
  - Once changes have been made in individual branches they can be **MERGED** with the **MASTER** branch and the feature branch can be deleted.

- **Merge Conflicts**
- Undoing add/commit in git
- **Forking**
   - making a **COPY** of another persons Repository as you dont have **ACCESS** to make changes(CRUD) to their Repo.
   - It creates your own local copy where you can make changes to the code.
   - If you want to add your changes to the original repository created by some other person then, you create a **pull** request.
   
---

## 🧪 Common Git Terms & Commands

- Directory --> Folder
- Terminal or Command Line --> Interface for typing text commands.
- CLI --> Command Line Interface.
- cd --> Change Directory.
- Repository --> Project/ folder where your project is kept.

| Command | Purpose |
|--------|---------|
| `clone` | Bring a repo down from the internet (remote repository like Github) to your local machine |
| `add` | Track your files and folders (update, create, delete) and changes with Git |
| `commit` | Save your changes into Git |
| `push` | Upload git commits from your local machine to a remote repository like Github |
| `pull` | Download changes from a remote repository to your local machine (opposite of **push**) |
| `status` | Gives all files and folders that were updated, created, deleted, but have not been committed yet |
| `init` | Makes a local folder into a **Git repository** by adding a hidden .git folder, which lets Git start tracking changes |
| `remote` | Just manages the connection between your **local repo** and a **remote repo** — doesn’t copy any code |
| `branch` | List existing branches, create new branches, and manage (rename, delete, or switch between branches) in your local Git project |
| `checkout` | Switch to a different branch or restore a specific file version in your project |
| `diff` | Shows the exact lines of code that have changed between your working directory, staging area, or branches |
| `merge` | Takes the work done in one branch and adds it into the branch you're currently on |

---

## 💻 Practice Log/ Code Trials

- Pulling a remote Repo to your local machine.
    1. Navigate to the directory where you want to clone your Repo.
    2. **git clone <SSH key>**
    3. Move into the newly pulled Repo using **cd <foldername>**
    4. Make changes to a file
    5. Check status of all the modified/untracked files that have not been committed yet using **git status**
    6. Track **all** the files (modified & untracked) using **git add .** or individual file/folder using **git add <filename>**
    7. **git status**
    8. Commit changes using **git commit -m"my message title"** or **git commit -m"my message title" -m"additional description"**. This saves changes in your local machine.
    9. To make the changes live in your remote Github repo use **git push origin main**

- Starting a Repo locally
   1. Navigate to the directory that you want to convert to a git Repo.
   2. **git init**
   3. **git status**
   4. **git add .**
   5. **git status**
   6. **git commit -m"my message title"**
   7. Create an empty git Repo on Github (where you will push your local Repo).
   8. **git remote add origin<SHH Key>**
   9. **git push origin main**

-Creating a branch
  1. **git branch**
  2. **git checkout -b new-branch**	: Creates and switches to a new branch
  3. **git checkout branch-name**	: Switches to another branch
  4. **git checkout filename.java** : Restores a file to last committed state
  5. modify data in new branch
  6. **git status**
  7. **git add .**
  8. **git commit -m"my message title"**
  9. **git checkout branch-name** --> changes will not be visible here.
  10. **git diff <branchname>** : Shows the differences between your current branch and the branch named branchname.
  11. **git checkout branch-name** : the branch you worked on.
  12. **git push -u origin branch-name** : pushing your branch to remote.
  13. Creating a **PULL REQUEST**.
  14. **git pull origin master** : pull changes to your local after merge
  15. **git branch -d branch-name** : remove the branch after use.

---

## 🧩 Reflection

- Vs Code Terminal for running git commands.
- Setting up SSH key.
- **.git** directory: **heart of every Git repository** - Stores full Git history, branches, config, and commits. If deleted	Your folder becomes a normal folder, no longer a Git repo.
- When you clone a GitHub repo, Git automatically names the original source **origin** by default.
- .gitignore and **git rm --cached Basic_Maths/CountDigits.class**
- git remote -v
- * indicates the branch you are currently on.
- git branch is local by default.
- **Pull request** : request to pull our code into another branch. e.g. request to pull the code of our branch into the main branch. Therefore make a PR from our branch to main branch



---
## 2. 📚 Git Handbook by GitHub

---
## 4. 📚 Learn Git Branching Game
 
---



