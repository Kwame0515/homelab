# Linux Lab 3 — Permissions & Ownership

## Objective
Practice Linux access control by viewing and changing file permissions, changing group and user ownership, and verifying results from the terminal.

## Environment
Kali Linux, terminal, working directory `~/PermissionLab`.

## Screenshot walkthrough
1. Created `PermissionLab` using `mkdir PermissionLab`, and created `report.txt` using `touch report.txt`.
2. Used `ls -l` to inspect permissions, owner, and group. Removed an initial `report.txt` from the home directory and worked inside `~/PermissionLab`.
3. Changed permissions with `chmod 777 report.txt`, resulting in `-rwxrwxrwx` (read, write, and execute for owner, group, and others).
4. Changed permissions to `770`, then `750`, checking each change with `ls -l`. The final `750` setting appears as `-rwxr-x---`.
5. Attempted `chgrp report.txt root`, which failed because the arguments were reversed: the command expects `chgrp GROUP FILE`.
6. Used `sudo chgrp root report.txt` and confirmed that the group changed to `root`.
7. Used `sudo chown root:root report.txt` to set both owner and group to `root`, confirmed with `ls -l`.

## Permission reference
| Mode | Owner | Group | Others |
| --- | --- | --- | --- |
| `777` | rwx | rwx | rwx |
| `770` | rwx | rwx | --- |
| `750` | rwx | r-x | --- |

`777` grants everyone full access and is generally inappropriate for sensitive files; this lab demonstrates its effect in a practice environment.

## Commands practiced
`mkdir`, `touch`, `cd`, `ls -l`, `chmod`, `chgrp`, `chown`, `sudo`, `rm`.

## Skills demonstrated
Linux file permissions, owner/group/other access interpretation, numeric permission modes, file ownership and group administration, elevated commands, verification, and troubleshooting.

## Key takeaway
Access permissions and file ownership are distinct controls. Use `ls -l` to validate changes, and grant only the access required.

*Documented from the Linux Lab 3 overview and terminal screenshot. Screenshot binary is not yet committed to this repository.*
