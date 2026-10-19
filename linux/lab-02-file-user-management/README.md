# Linux Lab 2 — File & User Management

## Objective
Practice Linux directory and file management, copying and renaming files, verifying user identity, switching to the root account, and cleaning up files.

## Environment
Kali Linux terminal, working directory `~/LinuxLab`.

## Terminal walkthrough
1. **Identify the account:** `whoami` returns `kowusu`.
2. **Create and enter a workspace:** `mkdir LinuxLab` and `cd LinuxLab`.
3. **Create files:** `touch notes.txt`, `touch tasks.txt`, and `touch inventory.txt`; `ls` verifies their presence.
4. **Edit and read files:** `nano notes.txt` and `cat notes.txt` display `Hello World!`.
5. **Copy a file:** An initial `cp notes.txt` fails because no destination was supplied. A later `cp notes.txt backupnotes.txt` succeeds, and `ls` confirms the backup.
6. **Rename a file:** `mv inventory.txt equipment.txt` changes the filename, confirmed with `ls`.
7. **Edit tasks:** `nano tasks.txt` opens the task file for editing.
8. **Switch accounts:** `sudo su` opens a root shell; `whoami` then returns `root`. `exit` is used to leave the elevated shell.
9. **Clean up:** `rm backupnotes.txt` removes the backup file.

## Troubleshooting observed
- `cd LinuxLab` while already inside `~/LinuxLab` fails because no nested `LinuxLab` folder exists.
- `cp notes.txt` fails without a destination.
- `cp notes.txt LinuxLab` fails because the relative destination `LinuxLab` does not exist in the current folder.
- `cp notes.txt notes.txt` fails because source and destination refer to the same file.

## Commands practiced
`mkdir`, `cd`, `touch`, `nano`, `cat`, `cp`, `mv`, `whoami`, `sudo su`, `exit`, `ls`, `rm`; the accompanying lab overview also lists `rmdir`.

## Skills demonstrated
File and directory organization, command-line editing, backup creation, renaming, troubleshooting relative paths, verifying account identity, working with elevated privileges, and file cleanup.

## Screenshot
Terminal screenshot supplied with the lab. The image will be linked here once the binary file is committed to the repository.

## Takeaway
Linux commands depend on the current working directory and the privileges of the active user. Confirm paths and identity before making changes, particularly in a root shell.
