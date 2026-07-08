# Commits

## Overview

A commit is a saved snapshot of staged changes in a Git repository.

Commits help track project history. Each commit records what changed, when it changed, and who made the change.

A clean commit history makes a repository easier to review, troubleshoot, and maintain.

```text
Working directory
      ↓
Staging area
      ↓
Commit
      ↓
Local repository
```

## Key concepts

| Term             | Description                              |
| ---------------- | ---------------------------------------- |
| Commit           | A saved snapshot of staged changes       |
| Commit message   | A short description of what changed      |
| Commit history   | The list of commits in a repository      |
| Commit hash      | A unique ID for each commit              |
| `HEAD`           | Pointer to the current commit            |
| Local repository | The place where commit history is stored |

## Why commits are used

Commits are used to save meaningful progress.

They help with:

* Tracking file changes
* Understanding project history
* Restoring older versions
* Reviewing work
* Debugging problems
* Sharing progress with others

A commit should represent one clear change.

Good example:

```text
Add staging area notes
```

Bad example:

```text
Update
```

The bad message gives almost no useful information. Classic human efficiency, but worse.

## Check current status

Before committing, check the repository status.

```bash
git status
```

This shows whether files are staged and ready to commit.

## Create a commit

Create a commit with a message:

```bash
git commit -m "Add commits notes"
```

The `-m` option is used to write the commit message directly in the command.

## View commit history

View detailed commit history:

```bash
git log
```

View commit history in one-line format:

```bash
git log --oneline
```

The one-line format is easier to scan.

Example output:

```text
a1b2c3d Add commits notes
9f8e7d6 Add staging area notes
5c4b3a2 Add working directory notes
```

## Commit message style

Use short and meaningful commit messages.

Good commit messages:

```text
Add Git architecture notes
Add installation notes
Add staging area notes
Update README progress
Fix repository structure table
```

Bad commit messages:

```text
Update
Done
Final
Changes
New file
```

A good commit message should explain the purpose of the change.

## Common commands

| Command                   | Description                          |
| ------------------------- | ------------------------------------ |
| `git status`              | Checks staged and unstaged changes   |
| `git add filename`        | Stages a specific file               |
| `git add .`               | Stages all changes                   |
| `git commit -m "message"` | Creates a commit with a message      |
| `git log`                 | Shows detailed commit history        |
| `git log --oneline`       | Shows commit history in short format |

## Example workflow

Check current status:

```bash
git status
```

Stage the file:

```bash
git add 07-commits.md
```

Check staged files:

```bash
git status
```

Create a commit:

```bash
git commit -m "Add commits notes"
```

View commit history:

```bash
git log --oneline
```

## Browser workflow

When using GitHub browser, commits are created after editing or creating a file.

Basic browser workflow:

```text
Open repository
Create or edit file
Preview changes
Write commit message
Commit changes
```

Use a clear commit message in the browser commit box.

Example:

```text
Add commits notes
```

Avoid vague commit messages such as:

```text
Update file
```

## Troubleshooting

| Issue                             | Cause                                  | Fix                                           |
| --------------------------------- | -------------------------------------- | --------------------------------------------- |
| Nothing to commit                 | No changes are staged                  | Use `git add filename` before committing      |
| Wrong file was committed          | Extra file was staged                  | Check `git status` before commit              |
| Commit message is unclear         | Message was too vague                  | Use a specific message                        |
| Commit does not appear on GitHub  | Commit was made locally but not pushed | Use `git push`                                |
| GitHub browser commit looks wrong | File was edited incorrectly            | Edit the file again and commit the correction |

## Notes

* A commit saves staged changes.
* A commit should describe one clear change.
* `git status` should be checked before committing.
* `git log --oneline` is useful for reviewing commit history.
* Clear commit messages make the repository easier to understand.
* Browser commits are acceptable for documentation, but command-line commits are better for learning Git workflow.
