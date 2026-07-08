# Git architecture

## Overview

Git has a clear workflow for tracking changes.

A file usually moves through these areas:

```text
Working directory
      ↓
Staging area
      ↓
Local repository
      ↓
Remote repository
```

Each area has a specific purpose. Understanding this flow makes Git commands easier to remember.

## Key concepts

| Term              | Description                                                 |
| ----------------- | ----------------------------------------------------------- |
| Working directory | The folder where files are created and edited               |
| Staging area      | The place where selected changes are prepared before commit |
| Local repository  | The Git history stored on the computer                      |
| Remote repository | The online copy of the repository, such as GitHub           |
| Commit            | A saved snapshot of staged changes                          |
| `HEAD`            | A pointer to the current commit                             |
| Branch            | A separate line of work inside the repository               |

## Working directory

The working directory is the project folder on the computer.

This is where files are:

* Created
* Edited
* Deleted
* Renamed

Git can detect changes in the working directory.

Check the current state:

```bash
git status
```

## Staging area

The staging area is where changes are prepared before committing.

Git does not automatically commit every file change. The user must choose which changes to include.

Add one file:

```bash
git add filename.md
```

Add all changed files:

```bash
git add .
```

Check staged files:

```bash
git status
```

## Local repository

The local repository stores committed history on the computer.

When changes are committed, Git saves a snapshot of the staged files.

Create a commit:

```bash
git commit -m "Add Git architecture notes"
```

View commit history:

```bash
git log --oneline
```

## Remote repository

A remote repository is an online copy of the local repository.

GitHub is commonly used as a remote repository platform.

A remote repository helps with:

* Backup
* Sharing code
* Collaboration
* Portfolio display
* Working from multiple systems

Common remote commands:

```bash
git remote -v
```

```bash
git push
```

```bash
git pull
```

## Basic Git workflow

The basic Git workflow is:

```text
Edit files
Stage changes
Commit changes
Push to GitHub
```

Command flow:

```bash
git status
```

```bash
git add .
```

```bash
git commit -m "Write clear commit message"
```

```bash
git push
```

## Example workflow

Create or edit a file:

```text
02-git-architecture.md
```

Check file status:

```bash
git status
```

Stage the file:

```bash
git add 02-git-architecture.md
```

Commit the staged file:

```bash
git commit -m "Add Git architecture notes"
```

Push the commit to GitHub:

```bash
git push
```

## Troubleshooting

| Issue                          | Cause                                   | Fix                                |
| ------------------------------ | --------------------------------------- | ---------------------------------- |
| File shows as untracked        | Git sees a new file that is not staged  | Use `git add filename`             |
| File shows as modified         | A tracked file was changed              | Stage and commit the change        |
| Commit does not include a file | The file was not staged before commit   | Use `git add` before committing    |
| Push fails                     | Remote repository may not be configured | Check remote using `git remote -v` |

## Notes

* The working directory is where editing happens.
* The staging area prepares selected changes.
* The local repository stores commit history.
* The remote repository stores the project online.
* `git status` is the most useful command for checking the current state.
* A commit only saves staged changes.
