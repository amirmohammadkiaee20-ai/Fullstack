# Git Commands

This document contains the essential Git commands I learned in Phase 0.
Each command is explained briefly with its real purpose in daily development.

## 🔹 Repository Setup

### Create New git Repository

Initializes a new Git repository in the current folder.

`git init`

### Clone a Repository

Clones an existing repository from GitHub to the local machine.

`git clone <repository-url>`

## 🔹 Checking Repository State

### git Status

Shows the current state of the working directory and staging area.

`git status`

### git Difference

Shows differences between the current working directory and the last commit.

`git diff HEAD`

### Commits History

Displays the commit history of the repository.

`git log`

### Show Detailed (Commit or Tag)

Shows detailed information about a specific commit or tag.

`git show <commithash-or-tagName>`

## 🔹 Staging & Committing

### Add File to Stage

Adds files to the staging area.

- All files:
  `git add -A`

- a particular file:
  `git add <file-name>`

### Create Commit

Creates a commit with a descriptive message.

`git commit -m "commit message"`

### Create Commit and Sign it

Creates a signed commit using a GPG key.

`git commit -S -m "signed commit message"`

### Restore from Stage

Removes files from the staging area (without deleting them).

`git reset <file-name>`

## 🔹 Removing Files

### Remove File

Removes files from both the working directory and Git tracking.

`git rm <file-name>`

## 🔹 Branching

### Show all Branches

Lists all branches in the repository.

`git branch`

### Create New Branch

Creates a new branch.

`git branch <Name>`

### Switch between Branches

Switches to another branch.

`git checkout <Branch-Name>`

### Merge Branches

Merges another branch into the current branch.

`git merge <Branch-Name>`

### Delete a Branch

Delete a branch.

`git branch -d <Branch-Name>`

## 🔹 Remote Repositories

### Connect to a local Repository

Connects a local repository to a remote repository.

`git remote add origin <repository-url>`

### Send Commits To Remote

Pushes local commits to the remote repository.

`git push origin main`

### Recive Changes from Remote

Fetches and integrates changes from the remote repository.

`git pull origin main`

## 🔹 Tags & Versioning

### Show all Tags

Lists all tags.

`git tag`

### Tag Lists (Pattern)

Lists tags matching a pattern.

`git tag -l "v*"`

### Create Tag with a Commit

Creates an annotated tag on the latest commit.

`git tag -a v1.0 -m "commit message"`

### Create Tag from Specific Commit

Creates an annotated tag on a specific commit.

`git tag -a v1.1 <commit-hash>`

### Create a Signed Tag

Creates a signed tag using a GPG key.

git tag -s v1.2 -m "commit message"

### Verify a Signed Tag

Verifies a signed tag.

`git tag -v v1.2`

## 🔹 GPG & Security

### Generate Key

Generates a new GPG key.

`gpg --gen-key`

### Show All Public Keys

Lists all public GPG keys.

`gpg --list-keys`

### Show All Secret Keys

Lists all secret GPG keys with long key IDs.

`gpg --list-secret-keys --keyid-format LONG`

### Config Signingkey

Change your user signing key.

`git config --global user.signingkey <key-id>`

## 🔹 Debugging & Investigation

### Show last modify

Shows who last modified each line of a file.

- All Lines:

`git blame <file-name>`

- Specific Lines:

`git blame <file-name> -L 10,20`

### Fixing Bug

Helps find the commit that introduced a bug.

`git bisect start`
`git bisect bad`
`git bisect good <commit-hash>`

## 🔹 Help

### git Help

Shows help for any Git command.

`git help <command>`
