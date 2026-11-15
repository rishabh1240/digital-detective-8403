# Mission 03 — Understand the Operating System

## 1. Task / Objective

The objective of this mission is to explore the operating system, understand running processes, examine storage information, learn about file paths and permissions, and identify the major responsibilities of an operating system.

In this mission, I used the macOS Terminal to explore system information, monitor running processes, and examine file permissions.

**Operating System:** macOS 27.2.1  
**Build Version:** 26B131  
**Terminal Shell:** Zsh

## 2. Work Completed

### Task 3.1 — Explore Your Operating System

I used Terminal commands to identify my operating system, check the current user account, examine storage information, and observe system activity.

**Commands Used**

| Command | Purpose |
|---|---|
| `sw_vers` | Displays macOS version and build information. |
| `whoami` | Displays the currently active username. |
| `df -h /` | Displays storage information for the root filesystem. |
| `df -h` | Displays storage information for mounted filesystems. |
| `top -l 1 -n 5` | Displays a snapshot of running processes and system resource usage. |

**Observations**

| Information Explored | My Observation |
|---|---|
| Operating System | macOS 27.2.1, Build 26B131 |
| Current Account Identity | Active account verified using `whoami`; username kept private. |
| Available and Used Storage | Root filesystem: 926 GiB capacity, 13 GiB used, 774 GiB available. |
| System Activity | 744 processes, 2 running, 742 sleeping, 91.73% CPU idle. |

**Additional Observations Using `top`**

- Total processes: 744
- Running processes: 2
- Sleeping processes: 742
- Total threads: 4074
- CPU usage by user processes: 1.95%
- CPU usage by system processes: 6.30%
- CPU idle: 91.73%
- Physical memory used: 22 GiB

The `df -h /` command displayed information about the root filesystem. Other mounted volumes, including the Data volume, were also visible using `df -h`.

### Task 3.2 — Understand Processes

A process is a program that is currently running on a computer. The operating system manages processes and allocates resources such as CPU time and memory to them.

**Command Used**

```bash
ps -ax -o pid,comm | head -n 15
```

**Command Explanation**

- `ps` — Displays information about running processes.
- `-a` — Includes processes associated with other users' terminals.
- `-x` — Includes processes without a controlling terminal.
- `-o pid,comm` — Displays the Process ID and command columns.
- `|` — Sends the output of one command to another.
- `head -n 15` — Displays only the first 15 lines of output.

**Processes Observed**

| PID | Process Name | Purpose |
|---|---|---|
| 1 | launchd | Starts and manages system services and processes. |
| 349 | logd | Collects and manages system log messages. |

These processes were observed running in the background on my MacBook. Process IDs may change between sessions.

**Questions and Answers**

**Q1. What is a process?**

A process is a program that is currently executing on a computer. Each process uses system resources such as CPU time and memory.

**Q2. What does the PID column represent?**

PID stands for Process ID. It is a unique number assigned to each running process. The operating system uses it to identify, monitor, and manage processes.

**Q3. Give two examples of processes running on your computer.**

1. **launchd (PID 1):** Responsible for starting and managing macOS system services.
2. **logd (PID 349):** Responsible for collecting and managing system logs.

### Task 3.3 — Understand Paths and Permissions

In this task, I explored file paths and examined file permissions using the macOS Terminal.

**Absolute Path**

An absolute path specifies the complete location of a file or directory, starting from the root directory `/`.

Example:

```text
/Users/[redacted]/Desktop/digital-detective-8403/mission-03-operating-system
```

**Relative Path**

A relative path specifies the location of a file or folder based on the current working directory.

Example:

```text
mission-03-operating-system
```

This relative path refers to the Mission 3 folder when the current directory is `digital-detective-8403`.

**Commands Used**

| Command | Purpose |
|---|---|
| `pwd` | Displays the current working directory. |
| `cd` | Changes the current directory. |
| `ls -l` | Displays detailed file and folder information, including permissions. |

**File Permissions**

I used the `ls -l` command to inspect the permissions of files and folders inside my assignment repository.

The root `README.md` file displayed the following permissions:

```text
-rw-r--r--
```

**Permission Explanation**

| Permission | Meaning | Owner Access |
|---|---|---|
| `r` — Read | Allows a file's contents to be read. | Allowed |
| `w` — Write | Allows a file to be modified. | Allowed |
| `x` — Execute | Allows a file to be executed. | Not allowed for README.md |

The permission string `-rw-r--r--` indicates that the file owner can read and write the file but cannot execute it. The group and other users have read permission only.

**Directory Permissions**

I also observed the following permissions for mission folders:

```text
drwxr-xr-x
```

Here, `d` indicates a directory.

The owner has read, write, and execute permissions. For directories, execute permission allows access or traversal. The group and other users have read and execute permissions.

No file or system permissions were changed during this task.

### Task 3.4 — Explain Operating-System Responsibilities

An operating system manages computer hardware, software resources, and provides services that allow applications to function.

**Major Responsibilities of an Operating System**

| OS Responsibility | My Explanation | Example |
|---|---|---|
| Process Management | The operating system manages running programs and allocates CPU time to different processes. | macOS allows Safari and VS Code to run simultaneously. |
| Memory Management | The operating system allocates and manages RAM for running applications. | macOS allocates memory to VS Code while editing files. |
| Device Management | The operating system controls hardware devices and manages communication between devices and applications. | macOS manages the keyboard, trackpad, and speakers. |
| File Management | The operating system organises, stores, retrieves, and manages files and folders. | Creating, renaming, and deleting files using Finder or Terminal. |
| User Interface / Shell | The operating system provides graphical and command-line interfaces for interacting with the computer. | macOS provides Finder and the Zsh command-line shell. |
| Security and Permissions | The operating system protects files and resources by controlling user access and permissions. | macOS uses read, write, and execute permissions to control file access. |

## 3. Commands / Tools Used

The following commands and tools were used throughout this mission:

| Command / Tool | Purpose |
|---|---|
| `sw_vers` | Checks macOS version and build information. |
| `whoami` | Identifies the current user. |
| `df -h /` | Checks root filesystem storage. |
| `df -h` | Displays mounted filesystem storage information. |
| `top -l 1 -n 5` | Observes processes and system resource usage. |
| `ps -ax -o pid,comm` | Displays process IDs and command names. |
| `head -n 15` | Limits output to the first 15 lines. |
| `pwd` | Displays the current directory. |
| `cd` | Changes the current directory. |
| `ls -l` | Displays file details and permissions. |
| macOS Terminal | Used to execute commands and inspect the operating system. |

## 4. My Understanding

Through this mission, I understood that an operating system acts as an interface between computer hardware, software, and users.

I learned that:

1. The operating system manages running processes and allocates CPU time.
2. Memory management ensures that applications receive the RAM they need.
3. File management helps organise, store, retrieve, and manage files.
4. Device management controls communication between hardware devices and applications.
5. Absolute paths provide complete file locations, whereas relative paths depend on the current working directory.
6. File permissions determine who can read, write, or execute files.
7. The operating system provides both graphical interfaces and command-line shells.

I also understood that many background processes run simultaneously and are managed by the operating system.

## 5. Difficulties Faced

**Difficulty 1: Understanding Filesystem Storage Information**

While using `df -h`, I observed multiple filesystem entries with different storage values, which made the output more difficult to interpret.

**Difficulty 2: Understanding Process Information**

The `top` command displayed a large amount of information about processes, CPU usage, memory, and other system resources.

## 6. How I Resolved Them

**Solution 1:**

I used `df -h /` to focus on the root filesystem and understood that macOS uses multiple mounted volumes.

**Solution 2:**

I used `ps -ax -o pid,comm | head -n 15` to display a shorter list containing process IDs and executable names, making the output easier to understand.

## 7. Evidence / Files

The following work and observations were included in this mission:

- `README.md` — Documentation of all four tasks.
- Terminal output from `sw_vers` and `whoami`.
- Storage information obtained using `df -h` and `df -h /`.
- Process information obtained using `top` and `ps`.
- File permissions observed using `ls -l`.
- Examples of absolute and relative paths.
- Operating-system responsibilities comparison table.

No passwords, tokens, or private system information are included.

## 8. Commit Details

**Suggested Commit Message:**

```bash
Document operating system and file management
```

The mission documentation should be staged, committed, and pushed to GitHub separately.

## 9. Conclusion

Mission 3 helped me understand how macOS manages processes, memory, storage, files, devices, and security.

By using Terminal commands and observing real system information, I gained practical knowledge of operating-system concepts and how they are applied in everyday computer usage.