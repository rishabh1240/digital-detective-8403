# Mission 00 — Create Your GitHub Workspace

## 1. Task / Objective

The objective of this mission was to create a local project workspace for **The Digital Detective — Diwali Independent Learning Assignment**, organise the required mission folders, and prepare the repository for version control using Git and GitHub.

## 2. Work Completed

- Created the project folder named `digital-detective-8403`.
- Created separate folders for all nine missions (Mission 00 to Mission 08).
- Created a `README.md` file inside every mission folder.
- Created the main `README.md` containing the project introduction and mission index.
- Created an `evidence` folder for supporting screenshots and outputs.
- Prepared the repository for uploading to GitHub.
- Published the repository on GitHub.

**Repository Name:** `digital-detective-8403`

**Repository Visibility:** Public

## 3. Commands / Tools Used

| Command / Tool | Purpose |
|---|---|
| `mkdir` | Create directories and folders. |
| `cd` | Navigate between directories. |
| `git init` | Initialise a Git repository. |
| `git remote add origin <repository-url>` | Connect the local repository to GitHub. |
| `git remote remove origin` | Remove an existing remote connection. |
| `git push origin main` | Push local commits to GitHub. |
| VS Code | Create and edit project files. |
| GitHub | Host the repository online. |
| Markdown | Document the project and mission activities. |

**Tools checked and versions:**

| Tool | Version |
|---|---|
| Python | 3.14.7 |
| Git | 2.54.0 (Apple Git-157) |

## 4. My Understanding

A repository is a storage space used to organise and manage project files. Git tracks changes made to these files, while GitHub allows repositories to be hosted online.

Organising a project into separate mission folders makes the work easier to manage, understand and review. README files provide documentation about the activities completed in each mission.

Git also helps maintain a history of changes, making it easier to track project progress and recover earlier versions.

## 5. Difficulties Faced

Initially, I encountered some difficulties while connecting my local repository to GitHub.

- I forgot to specify the remote name `origin` while adding the remote repository.
- I received an error while pushing because the remote repository already contained files that were not present locally.
- I also encountered an error stating that the remote `origin` already existed when I tried adding it again.

## 6. How I Resolved Them

- Corrected the remote command by specifying `origin` along with the repository URL.
- Used `git remote remove origin` to remove the existing remote connection.
- Added the remote repository again using the correct URL.
- Attempted to push the project using `git push origin main`.

Through these steps, I understood how to configure remote repositories and resolve common Git errors.

## 7. Evidence / Files

The following files and folders were created as part of this mission:

- `README.md` — Main project introduction and mission index.
- `mission-00-setup/README.md`
- `mission-01-computer-basics/README.md`
- `mission-02-terminal/README.md`
- `mission-03-operating-system/README.md`
- `mission-04-programs/README.md`
- `mission-05-numbers-data/README.md`
- `mission-06-git-github/README.md`
- `mission-07-networking/README.md`
- `mission-08-final-report/README.md`
- `evidence/` — Folder for supporting evidence.

## 8. Commit Details

**Commit Message:** `Set up Digital Detective mission structure`

The initial project structure was committed using Git and pushed to the GitHub repository.

The repository was published publicly, and the project files were made available on GitHub.