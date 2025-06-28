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
  
- **Git** vs **Github**
  Git: Tool for tracking changes in your code overtime.
  Github: Website to host your Git repositories, so that you can work online in teams an organise your projects in a portfolio.
  
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
| `status` | gives all files and folders that were updated, created, deleted, but have not been committed yet |

---

## 💻 Practice Log/ Code Trials

> ✨ Will document what i tried and what i observed.

---

## 🧩 Reflection

- Always run `git status` before committing — it’s your friend 🟢

---
## 2. 📚 Git Handbook by GitHub

---

## 3. 📚 Codecademy – Learn Git

---

## 4. 📚 Learn Git Branching Game
 
---



