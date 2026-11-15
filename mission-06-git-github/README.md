# Mission 6 — Git and GitHub

## Mission Objective

Understand version control, stage and commit changes, create and use branches, open a Pull Request and explain the GitHub collaboration workflow.

## Task 6.1 — Understand the Basic Git Workflow

I explored the basic Git workflow using my assignment repository.

### Git Operations

| Git Operation | Command | What It Does |
|---|---|---|
| Check repository status | `git status` | Shows modified, staged and untracked files. |
| Stage selected changes | `git add filename` | Selects specific changes for the next commit. |
| Create a commit | `git commit -m "message"` | Records staged changes in the repository history. |
| View commit history | `git log --oneline` | Displays previous commits in a short format. |

### Difference Between Staging and Committing

Staging means selecting the changes that I want to include in the next commit. Committing means saving those staged changes as a recorded version in Git history.

## Task 6.2 — Create and Use a Branch

I created a new branch named `update-about` using Git.

### Commands Used

```bash
git branch update-about
git switch update-about
```

I opened the root `README.md` file and added a section titled **My Learning**.

### My Learning

During this assignment, I learned several important concepts:

1. **Computer and Operating Systems:** Understanding the IPOS cycle, hardware, software and operating-system responsibilities.

2. **Terminal and Python:** Using Terminal commands to navigate directories and manage files, understanding processes, writing Python programs and performing number conversions.

3. **Git and GitHub:** Understanding version control, staging and committing changes, maintaining commit history, creating branches and collaborating through Pull Requests.

After updating the README, I checked the repository status, staged the changes, committed them and published the new branch.

### Commands Used

```bash
git status
git add README.md
git commit -m "Add My Learning section"
git push -u origin update-about
```

## Task 6.3 — Create a Pull Request

I used GitHub to create a Pull Request from the `update-about` branch into the `main` branch.

### Steps Followed

1. Opened my repository on GitHub.
2. Located the option to compare the recently published `update-about` branch with the `main` branch.
3. Created a Pull Request from `update-about` into `main`.
4. Added a short description explaining the changes made to the README.

### Pull Request Description

This Pull Request introduces a new "My Learning" section in the root README.md file. It summarizes the key concepts and skills I learned throughout the assignment, including computer fundamentals, operating systems, Terminal commands, Python programming, Git and GitHub.

5. Reviewed the changed file in the Pull Request. Merging is done only if instructed by the instructor.
6. After merging, the local project can be updated by switching to the main branch and retrieving the latest changes.

### Commands to Update the Local Main Branch

```bash
git switch main
git pull origin main
```

### What Is a Branch?

A branch is a separate line of development in a Git repository. It allows developers to work on new features or changes without directly affecting the main branch.

### What Is a Pull Request?

A Pull Request (PR) is a request to review and merge changes from one branch into another. It allows collaborators to discuss, review and approve changes before they become part of the main project.

### Why Are Branches and Pull Requests Useful?

Branches allow multiple people to work on different tasks independently without disturbing the main project. Pull Requests help review changes, identify mistakes, discuss improvements and maintain better collaboration when people work on the same project.

## Task 6.4 — Git Command Glossary

The following table explains the important Git operations in my own words.

| Git Operation | Command | Explanation |
|---|---|---|
| Initialise a repository | `git init` | Creates a new Git repository in the current folder. |
| Check status | `git status` | Shows the current state of files and changes. |
| Stage changes | `git add .` | Stages all changes in the current directory. |
| Commit changes | `git commit -m "message"` | Saves staged changes in the repository history. |
| View history | `git log --oneline` | Displays previous commits and their messages. |
| Create a branch | `git branch branch-name` | Creates a new branch. |
| List branches | `git branch` | Displays the available local branches. |
| Switch branches | `git switch branch-name` | Moves from one branch to another. |
| Publish changes | `git push origin branch-name` | Uploads local commits to the remote GitHub repository. |
| Retrieve remote changes | `git pull origin branch-name` | Downloads and integrates the latest changes from the remote branch. |

## What I Learned

Through this mission, I understood how Git tracks changes and how GitHub hosts repositories for collaboration. I learned the importance of staging, committing and maintaining commit history. I also practised creating a separate branch, publishing it to GitHub and opening a Pull Request to propose changes.

### Difficulties Faced

Initially, I encountered some confusion while understanding the difference between staging, committing and pushing changes. I resolved this by practising the Git commands and observing how the repository status and commit history changed after each operation.

## Conclusion

Mission 6 helped me understand the Git version-control workflow and how GitHub supports collaboration. I learned how to manage changes safely using branches and Pull Requests while keeping the main project organised.