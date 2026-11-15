# Mission 02 — Become Comfortable with the Terminal

## 1. Mission Title and Objective

**Mission:** Become Comfortable with the Terminal

The objective of this mission is to understand and practise basic terminal operations, file management, command-line flags, pipes, and package managers.

Through this mission, I learned how to navigate directories, create and manage files, use terminal commands with different options, and explore Homebrew on macOS.

**Operating System:** macOS  
**Terminal Shell:** Zsh  
**Package Manager:** Homebrew 7.0.9

## 2. Work Completed

### Task 2.1 — Explore Basic Terminal Operations

In this task, I practised basic terminal commands to navigate directories, create files and folders, copy files, rename files, and display file contents.

| Operation / Command | What It Does | What I Observed |
|---|---|---|
| `pwd` | Displays the current working directory | Displayed the full path of my project folder |
| `ls` | Lists files and folders in the current directory | Displayed the folders and files in my repository |
| `ls -l` | Displays a detailed directory listing | Showed file permissions, ownership, sizes, and modification dates |
| `cd ..` | Moves to the parent directory | Changed my location from the project folder to Desktop |
| `mkdir practice` | Creates a new directory | Created a folder named practice |
| `touch rishabh.txt` | Creates an empty text file | Created a new empty file |
| `cp rishabh.txt ansh.txt` | Copies a file | Created a copy named ansh.txt |
| `mv rishabh.txt aryan.txt` | Renames or moves a file | Renamed rishabh.txt to aryan.txt |
| `cat aryan.txt` | Displays the contents of a file | Displayed no text because the file was empty |

**Explanation**

The `pwd` command helped me identify my current location in the file system. The `ls` and `ls -l` commands displayed files and their details.

Using `cd ..`, I moved from my project directory to its parent directory. I then created a practice folder and performed file operations using `touch`, `cp`, and `mv`.

The `cat` command produced no text because the file was empty.

### Task 2.2 — Practise File Changes Safely

In this task, I practised writing text into a file, appending additional text, creating a backup copy, and renaming the backup.

**1. Create a practice directory and text file**

```bash
mkdir terminal-practice
cd terminal-practice
touch rishabh.txt
```

**2. Write the first line into the file**

```bash
echo "Rishabh is in Bengaluru" > rishabh.txt
```

**3. Append the second line**

```bash
echo "Ansh is in Ranchi" >> rishabh.txt
```

**4. Display the file contents**

```bash
cat rishabh.txt
```

**Output:**

```text
Rishabh is in Bengaluru
Ansh is in Ranchi
```

**5. Create a backup copy**

```bash
cp rishabh.txt bacup.txt
```

**6. Rename the backup**

```bash
mv bacup.txt rishabh-backup.txt
```

**Questions and Answers**

**Q1. What is the difference between replacing a file's contents and adding text to the end?**

The `>` operator writes text into a file by replacing its existing contents, while the `>>` operator appends new text to the end without deleting the existing content.

**Q2. What is the difference between copying a file and moving a file?**

The `cp` command creates a duplicate file while keeping the original unchanged. The `mv` command moves a file to another location or renames it without creating a separate copy.

**Q3. What information does the current-directory display provide?**

The `pwd` command displays the absolute path of the current working directory. It helps identify the location where terminal commands are being executed.

**Q4. Why is a directory-listing operation useful?**

Directory listing helps users view available files and folders, check filenames, and organise files efficiently.

### Task 2.3 — Understand Flags and Pipes

In this task, I explored how command-line flags modify the behaviour of commands and how pipes connect multiple commands.

**Commands Used**

| Command | Purpose | Observation |
|---|---|---|
| `ls` | Displays a normal directory listing | Displayed rishabh.txt and rishabh-backup.txt |
| `ls -l` | Displays detailed information | Showed file permissions, sizes, ownership, and dates |
| `ls -a` | Includes hidden files and directories | Displayed additional entries such as `.` and `..` |
| `ls -h` | Enables human-readable file sizes when sizes are displayed | Displayed filenames without detailed size information |
| `ls -lh` | Displays detailed information with human-readable sizes | Showed both text files with sizes of 42B |
| `ls -l \| head -n 1` | Displays the first line of the detailed listing | Displayed only `total 16` |
| `ls -l \| head -n 2` | Displays the first two lines of the detailed listing | Displayed `total 16` and the first file entry |

**Explanation of Flags**

A flag is an option added to a command to modify its behaviour.

- `-l` displays detailed file information.
- `-a` includes hidden files and directories.
- `-h` makes displayed file sizes easier to read using units such as B, K, M, and G.

For example:

```bash
ls -lh
```

This command combines two flags to display a detailed directory listing with human-readable file sizes.

**Understanding Pipes**

A pipe (`|`) sends the output of one command as input to another command.

**Command executed:**

```bash
ls -l | head -n 2
```

The `ls -l` command generates a detailed directory listing, while `head -n 2` displays only the first two lines of that output.

**What I Observed**

The normal `ls` command displayed only filenames, while `ls -l` provided additional details.

The `ls -a` command displayed hidden entries, and `ls -lh` displayed both text files with human-readable sizes of 42B.

When I used a pipe with `head`, the terminal displayed only the requested number of lines instead of the complete listing.

### Task 2.4 — Understand Package Managers

A package manager is a software tool used to install, update, remove, and manage software packages and their dependencies.

On macOS, Homebrew is a commonly used package manager.

**Commands Used**

| Command | Purpose | Observation |
|---|---|---|
| `brew --version` | Checks the Homebrew version | Displayed Homebrew 7.0.9 |
| `brew -h` | Displays Homebrew help information | Showed available commands and their usage |
| `brew list` | Lists installed Homebrew packages | Displayed packages installed on my MacBook |

**Packages Observed**

Some packages displayed by `brew list` included:

- git
- ffmpeg
- ruby
- openssl@3
- openssl@4
- x264
- x265
- libpng
- gettext
- pcre2

**Why Are Package Managers Useful?**

Package managers simplify the process of installing, updating, and removing software. They help manage dependencies automatically and reduce the need to download and configure software manually.

They also make software maintenance more efficient by providing a centralised way to manage installed packages.

**What I Observed**

Homebrew was already installed on my MacBook, with version 7.0.9.

I successfully viewed the available Homebrew commands and checked the list of installed packages.

I did not install or uninstall any software during this task.

## 3. Commands / Tools Used

| Command / Tool | Purpose |
|---|---|
| `pwd` | Displays the current working directory |
| `ls` | Lists files and directories |
| `ls -l` | Displays detailed file information |
| `ls -a` | Displays hidden files and directories |
| `ls -h` | Enables human-readable size formatting |
| `ls -lh` | Displays detailed information with human-readable sizes |
| `cd ..` | Moves to the parent directory |
| `mkdir` | Creates directories |
| `touch` | Creates empty files |
| `cp` | Copies files |
| `mv` | Moves or renames files |
| `cat` | Displays file contents |
| `echo` | Writes or appends text |
| `head` | Displays the first specified number of lines |
| `brew --version` | Checks the Homebrew version |
| `brew -h` | Displays Homebrew help |
| `brew list` | Lists installed Homebrew packages |
| `Terminal (Zsh)` | Used to execute commands on macOS |
| `Homebrew` | Package manager used to explore installed software |

## 4. My Understanding

Through this mission, I understood how to navigate the file system and perform basic file-management operations using the Terminal.

I learned that the `>` operator overwrites existing file contents, whereas `>>` appends text without deleting existing content.

I also understood how command-line flags modify command behaviour and how pipes connect commands to filter output.

Finally, I learned that package managers such as Homebrew simplify software installation, updating, and dependency management.

## 5. Difficulties Faced

**Difficulty 1: Understanding Human-Readable File Sizes**

Initially, I used `ls -h` expecting it to display file sizes. However, it only displayed filenames.

**Difficulty 2: Understanding Pipe Output**

When I executed `ls -l | head -n 1`, the output displayed only `total 16` instead of a filename.

## 6. How I Resolved Them

**Solution 1:** I used `ls -lh`, which combines the detailed listing flag with the human-readable flag. This displayed the file sizes as 42B.

**Solution 2:** I understood that `head` counts all output lines, including the total line. Using `head -n 2` displayed the total line and the first file entry.

These exercises helped me understand command options and how commands work together through pipes.

## 7. Evidence / Files

The following files and folders were created or used during this mission:

- `mission-02-terminal/README.md` — Documentation of terminal activities and observations.
- `terminal-practice/` — Folder containing terminal practice work.
- `rishabh.txt` — Text file containing two lines of text.
- `rishabh-backup.txt` — Backup copy of the original text file.

The practice files were created using Terminal commands and used to understand file operations.

## 8. Commit Details

**Commit Message:** `Mission 02 Completed`

The completed Mission 02 documentation and terminal activities were committed using Git and pushed to the GitHub repository.

## 9. Conclusion

Mission 2 helped me become more comfortable using the macOS Terminal. By performing practical activities, I developed a better understanding of file management, directory navigation, command-line flags, pipes, and package managers.

These skills will be useful for future programming, operating system, and Git-related activities in this assignment.