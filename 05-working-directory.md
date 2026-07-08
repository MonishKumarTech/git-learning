# Working directory

## Overview

The working directory is the project folder where files are created, edited, renamed, or deleted.

Git watches the working directory and detects changes in tracked and untracked files.

The working directory is the first stage in the Git workflow.

```text
Working directory
      ↓
Staging area
      ↓
Local repository
```

## Key concepts

| Term               | Description                                    |
| ------------------ | ---------------------------------------------- |
| Working directory  | The project folder where file changes happen   |
| Untracked file     | A new file that Git is not tracking yet        |
| Modified file      | A tracked file that has been changed           |
| Deleted file       | A tracked file that has been removed           |
| Staged file        | A file prepared for commit                     |
| Clean working tree | A state where there are no uncommitted changes |

## File states in the working directory

Git uses file states to show what has changed.

| State     | Meaning                                    |
| --------- | ------------------------------------------ |
| Untracked | Git sees a new file but is not tracking it |
| Modified  | A tracked file has been changed            |
| Deleted   | A tracked file has been removed            |
| Staged    | A file is prepared for commit              |
| Committed | A file change is saved in Git history      |

## Check working directory status

Use `git status` to check the current state of files.

```bash
git status
```

This command shows:

* Current branch
* Untracked files
* Modified files
* Deleted files
* Staged files
* Whether the working tree is clean

## Example: untracked file

Create a new file:

```bash
touch notes.md
```

Check status:

```bash
git status
```

Example output:

```text
Untracked files:
  notes.md
```

This means Git sees the file, but it is not tracking it yet.

## Example: modified file

Edit an existing tracked file.

Check status:

```bash
git status
```

Example output:

```text
Changes not staged for commit:
  modified: README.md
```

This means the file is tracked, but the latest change has not been staged.

## Example: deleted file

Delete a tracked file.

Check status:

```bash
git status
```

Example output:

```text
Changes not staged for commit:
  deleted: old-notes.md
```

This means Git has detected that a tracked file was removed.

## Common commands

| Command                         | Description                                      |
| ------------------------------- | ------------------------------------------------ |
| `git status`                    | Shows the current state of the working directory |
| `git add filename`              | Stages a specific file                           |
| `git add .`                     | Stages all changes in the current directory      |
| `git restore filename`          | Discards changes in a modified file              |
| `git restore --staged filename` | Removes a file from the staging area             |

## Example workflow

Check the current status:

```bash
git status
```

Create a file:

```bash
touch working-directory-notes.md
```

Check status again:

```bash
git status
```

Stage the file:

```bash
git add working-directory-notes.md
```

Check staged status:

```bash
git status
```

Commit the file:

```bash
git commit -m "Add working directory notes"
```

## Browser workflow

When using GitHub browser, the working directory is not visible in the same way as command-line Git.

In the browser, file changes are usually committed directly after editing.

Basic browser workflow:

```text
Open file
Edit content
Preview changes
Commit changes
```

This is useful for documentation, but it hides the working directory and staging area. Command-line Git shows these stages more clearly.

## Troubleshooting

| Issue                     | Cause                                | Fix                                                          |
| ------------------------- | ------------------------------------ | ------------------------------------------------------------ |
| File appears as untracked | The file is new and not added to Git | Use `git add filename`                                       |
| File appears as modified  | A tracked file was edited            | Stage and commit the change                                  |
| Wrong file was changed    | The file was edited by mistake       | Use `git restore filename` if the change should be discarded |
| Nothing to commit         | No changes are staged                | Use `git add` before committing                              |
| Working tree is clean     | There are no pending changes         | No action is required                                        |

## Notes

* The working directory is where file editing happens.
* `git status` should be used often.
* Untracked files are not included in commits until they are staged.
* Modified files must be staged before committing.
* The working directory is easier to understand when using Git commands instead of only the GitHub browser.
