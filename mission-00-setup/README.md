# Mission 0 — Create Your GitHub Workspace

## 1. Task Completed

In this mission, I created a local project workspace for **The Digital Detective — Diwali Independent Learning Assignment**.

I organised the project into separate folders for each mission and created the required README.md files to document my work.

**Repository Name:** `digital-detective-8403`

**Repository Visibility:** Public (after publishing)

## 2. Tools Checked and Their Versions

The following tools were used for this assignment:

| Tool | Version |
|---|---|
| Python | 3.14.7 |
| Git | 2.54.0 (Apple Git-157) |

## 3. Folders and Files Created

I created the following project structure:

- `README.md` — Main project introduction and mission index.
- `mission-00-setup/` — GitHub workspace setup.
- `mission-01-computer-basics/` — Computer fundamentals.
- `mission-02-terminal/` — Terminal commands and activities.
- `mission-03-operating-system/` — Operating system concepts.
- `mission-04-programs/` — Python programs.
- `mission-05-numbers-data/` — Number conversions and data.
- `mission-06-git-github/` — Git and GitHub activities.
- `mission-07-networking/` — Networking concepts.
- `mission-08-final-report/` — Final review and submission.
- `evidence/` — Screenshots and supporting evidence.

The required Markdown files and `number_converter.py` file were also created.

## 4. What Is a Repository?

A repository is a storage space used to organise and manage project files. Git tracks changes made to these files, while GitHub allows repositories to be hosted online.

Repositories help maintain version history, organise work, and share projects with others.

## 5. Why Is the Folder Structure Organised by Mission?

The project is divided into separate mission folders to keep the work organised and easy to understand.

Each mission has its own README.md file containing explanations, activities, and observations.

This structure makes it easier to locate files, track progress, and review completed tasks.

## 6. Setup Difficulties and Solutions

**Difficulty:** While connecting my local project to GitHub, I initially received an error because I forgot to specify the remote name `origin` in the `git remote add` command. After correcting it, I encountered another error while pushing my project because the remote repository already contained files that were not present locally. I also received an error stating that the remote `origin` already existed when I tried adding it again.

**Solution:** I corrected the remote command by specifying `origin` along with the repository URL. To resolve the duplicate remote error, I removed the existing remote using `git remote remove origin` and added it again with the correct URL. I then attempted to push my project to GitHub again using `git push origin main`.

**Learning Outcome:** Through this process, I learned how to connect a local Git repository to GitHub, configure and remove remote repositories, and understand common Git errors while pushing code.

## 7. Git Commit and GitHub Submission

Each mission will be completed and committed separately using Git.

After completing Mission 0, the setup files will be committed with the message:

`Set up Digital Detective mission structure`

The repository will then be pushed to GitHub and checked to ensure all required files are visible.

## 8. Conclusion

Through this mission, I learned how to organise a project workspace, create a repository structure, prepare Markdown documentation, and use Git and GitHub for version control.