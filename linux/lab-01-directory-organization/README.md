# Linux Lab 1 — User Directory Organization

## Objective
Practice navigating the Linux filesystem, creating and editing files, and verifying directory contents in a Kali Linux terminal.

## Lab environment
- Kali Linux
- Terminal, Nano text editor
- Working directory: `~/Desktop/project`

## Screenshot walkthrough
The supplied terminal screenshot demonstrates the following sequence:

1. **Navigate to the parent folder:** `cd ..` moves from `~/Desktop/project/notes` to `~/Desktop/project`.
2. **Create a file:** `touch index.txt` creates the project-level text file.
3. **Verify contents:** `ls` displays `index.txt` and the `notes` directory.
4. **Edit files:** `nano index.txt` and `nano README.md` open files in a terminal-based editor.
5. **Inspect file contents:** `cat README.md` displays `Hello World`, and `cat index.txt` displays `This is the index`.
6. **Troubleshoot relative paths:** Running `cat index.txt` inside `notes` returns `No such file or directory` because `index.txt` is in the parent directory. Returning with `cd ..` allows the command to succeed.

## Directory structure
```text
~/Desktop/project/
├── index.txt
└── notes/
    └── README.md
```

## Commands practiced
`pwd`, `ls`, `cd`, `mkdir`, `touch`, `nano`, `cat`

## Skills demonstrated
Linux filesystem navigation, directory organization, text-file creation, terminal editing, output verification, relative-path troubleshooting.

## Key takeaway
Commands that use relative file paths depend on the current working directory. When a file cannot be found, verify your location with `pwd` and inspect the directory with `ls`.

*Based on the Linux Lab 1 overview and terminal screenshot.*
