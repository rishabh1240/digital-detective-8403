# Mission 03 — Understand the Operating System

## Mission Objective

The objective of this mission is to explore the operating system, understand running processes, examine storage information, learn about file paths and permissions, and identify the major responsibilities of an operating system.

In this mission, I used the macOS Terminal to explore system information, monitor running processes, and examine file permissions.

**Operating System:** macOS 27.2.1  
**Build Version:** 26B131  
**Terminal Shell:** Zsh

---

## Task 3.1 — Explore Your Operating System

In this task, I used Terminal commands to identify my operating system, check the current user account, examine storage information, and observe system activity.

### Commands Used

| Command | Purpose |
|---|---|
| `sw_vers` | Displays macOS version and build information |
| `whoami` | Displays the currently active username |
| `df -h /` | Displays storage information for the root filesystem |
| `df -h` | Displays storage information for mounted filesystems |
| `top -l 1 -n 5` | Displays a snapshot of running processes and system resource usage |

### Observations

| Information Explored | What It Tells You | My Observation (Privacy-Safe) |
|---|---|---|
| Operating System / System Details | Identifies the installed operating system and its version | macOS 27.2.1, Build 26B131 |
| Current Account Identity | Identifies the currently active user account | Active account verified using `whoami`; username [redacted] |
| Available and Used Storage | Shows filesystem capacity and storage usage | Root filesystem: 926 GiB capacity, 13 GiB used, 774 GiB available |
| System Activity Snapshot | Displays running processes, CPU usage, and memory information | 744 processes, 2 running, 742 sleeping, 91.73% CPU idle |

### Additional Observations

Using the `top` command, I observed:

- Total processes: 744
- Running processes: 2
- Sleeping processes: 742
- Total threads: 4074
- CPU usage by user processes: 1.95%
- CPU usage by system processes: 6.30%
- CPU idle: 91.73%
- Physical memory used: 22 GiB

The `df -h /` command displayed information about the root filesystem. Other mounted volumes, including the Data volume, were also visible using `df -h`.

### What I Learned

I learned how to identify operating-system details, check the active user account, view filesystem storage information, and monitor system activity through Terminal commands.

---

## Task 3.2 — Understand Processes

A process is a program that is currently running on a computer. The operating system manages processes and allocates resources such as CPU time and memory to them.

### Command Used

```bash
ps -ax -o pid,comm | head -n 15
```

### Command Explanation

- `ps` — Displays information about running processes.
- `-a` — Includes processes associated with other users' terminals.
- `-x` — Includes processes without a controlling terminal.
- `-o pid,comm` — Displays the Process ID and command columns.
- `|` — Sends the output of one command to another.
- `head -n 15` — Displays only the first 15 lines of output.

### Processes Observed

| PID | Process Name | Purpose |
|---|---|---|
| 1 | launchd | Starts and manages system services and processes |
| 349 | logd | Collects and manages system log messages |

These processes were observed running in the background on my MacBook.

### Questions and Answers

**Q1. What is a process?**

A process is a program that is currently executing on a computer. Each process uses system resources such as CPU time and memory.

**Q2. What does the PID column represent?**

PID stands for Process ID. It is a unique number assigned to each running process. The operating system uses it to identify, monitor, and manage processes.

**Q3. Give two examples of processes running on your computer.**

Two processes observed were:

1. **launchd (PID 1):** Responsible for starting and managing macOS system services.
2. **logd (PID 349):** Responsible for collecting and managing system logs.

Process IDs may change between sessions.

### What I Learned

I learned that many processes run simultaneously on a computer, including background system services. Each process has a PID that helps the operating system identify and manage it.

---

## Task 3.3 — Understand Paths and Permissions

In this task, I explored file paths and examined file permissions using the macOS Terminal.

### Absolute and Relative Paths

**Absolute Path:**

An absolute path specifies the complete location of a file or directory, starting from the root directory `/`.

Example:

```text
/Users/[redacted]/Desktop/digital-detective-8403/mission-03-operating-system
```

**Relative Path:**

A relative path specifies the location of a file or folder based on the current working directory.

Example:

```text
mission-03-operating-system
```

This relative path refers to the Mission 3 folder when the current directory is `digital-detective-8403`.

### Commands Used

| Command | Purpose |
|---|---|
| `pwd` | Displays the current working directory |
| `cd` | Changes the current directory |
| `ls -l` | Displays detailed file and folder information, including permissions |

### File Permissions

I used the `ls -l` command to inspect the permissions of files and folders inside my assignment repository.

The root `README.md` file displayed the following permissions:

```text
-rw-r--r--
```

### Permission Explanation

| Permission | Meaning | Owner Access |
|---|---|---|
| `r` — Read | Allows a file's contents to be read | Allowed |
| `w` — Write | Allows a file to be modified | Allowed |
| `x` — Execute | Allows a file to be executed | Not allowed for README.md |

The permission string `-rw-r--r--` indicates that the file owner can read and write the file but cannot execute it. The group and other users have read permission only.

### Directory Permissions

I also observed the following permissions for mission folders:

```text
drwxr-xr-x
```

Here, `d` indicates a directory.

The owner has read, write, and execute permissions. For directories, execute permission allows access or traversal.

The group and other users have read and execute permissions.

No file or system permissions were changed during this task.

### What I Learned

I learned the difference between absolute and relative paths and understood how file permissions control access to files and directories.

---

## Task 3.4 — Explain Operating-System Responsibilities

An operating system manages computer hardware, software resources, and provides services that allow applications to function.

### Major Responsibilities of an Operating System

| OS Responsibility | My Explanation | Example |
|---|---|---|
| Process Management | The operating system manages running programs and allocates CPU time to different processes. | macOS allows Safari and VS Code to run simultaneously. |
| Memory Management | The operating system allocates and manages RAM for running applications. | macOS allocates memory to VS Code while editing files. |
| Device Management | The operating system controls hardware devices and manages communication between devices and applications. | macOS manages the keyboard, trackpad, and speakers. |
| File Management | The operating system organises, stores, retrieves, and manages files and folders. | Creating, renaming, and deleting files using Finder or Terminal. |
| User Interface / Shell | The operating system provides graphical and command-line interfaces for interacting with the computer. | macOS provides Finder and the Zsh command-line shell. |
| Security and Permissions | The operating system protects files and resources by controlling user access and permissions. | macOS uses read, write, and execute permissions to control file access. |

### What I Learned

I learned that an operating system performs important functions such as managing processes, allocating memory, controlling hardware devices, organising files, providing user interfaces, and maintaining security.

These responsibilities allow computers to run applications efficiently and securely.

---

## Difficulties Faced and Solutions

**Difficulty 1: Understanding Filesystem Storage Information**

While using `df -h`, I observed multiple filesystem entries with different storage values, which made the output more difficult to interpret.

**Solution:** I used `df -h /` to focus on the root filesystem and understood that macOS uses multiple mounted volumes.

**Difficulty 2: Understanding Process Information**

The `top` command displayed a large amount of information about processes, CPU usage, memory, and other system resources.

**Solution:** I used `ps -ax -o pid,comm | head -n 15` to display a shorter list containing process IDs and executable names, making the output easier to understand.

---

## Overall Learning Outcomes

After completing Mission 3, I learned:

1. How to identify operating-system information using Terminal commands.
2. How to check filesystem storage and system activity.
3. How to view running processes and understand Process IDs.
4. The difference between absolute and relative paths.
5. How read, write, and execute permissions work.
6. The major responsibilities of an operating system.

## Conclusion

Mission 3 helped me understand how macOS manages processes, memory, storage, files, devices, and security.

By using Terminal commands and observing real system information, I gained practical knowledge of operating-system concepts and how they are applied in everyday computer usage.