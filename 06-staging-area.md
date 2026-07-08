# Staging area

## Overview

The staging area is the place where selected changes are prepared before creating a commit.

Git does not automatically commit every change from the working directory. The user must choose which files or changes should be included in the next commit.

The staging area gives control over what becomes part of the commit.

```text
Working directory
      ↓
Staging area
      ↓
Local repository
```

## Key concepts

| Term            | Description                                                               |
| --------------- | ------------------------------------------------------------------------- |
| Staging area    | The place where selected changes are prepared before commit               |
| Staged file     | A file added to the staging area                                          |
| Unstaged change | A change that exists in the working directory but is not ready for commit |
| Commit          | A saved snapshot of staged changes                                        |
| `git add`       | Command used to move changes into the staging area                        |

## Why staging is used

The staging area is useful because it allows selective commits.

Instead of committing all changes at once, Git allows the user to choose only the required files.

This helps create clean and meaningful commit history.

Example:

```text
README.md changed
06-staging-area.md changed
test-file.txt changed
```

If only `06-staging-area.md` is related to the current topic, only that file should be staged and committed.

## Check file status

Use `git status` to check which files are staged and unstaged.

```bash
git status
```

This command shows:

* Untracked files
* Modified files
* Staged files
* Files ready to commit

## Stage one file

Stage a specific file:

```bash
git add 06-staging-area.md
```

This adds only `06-staging-area.md` to the staging area.

## Stage all changes

Stage all changed files:

```bash
git add .
```

This stages all changes in the current directory.

Use this carefully. It may include files that should not be committed.

## Stage multiple specific files

Stage selected files:

```bash
git add README.md 06-staging-area.md
```

This stages only the listed files.

## View staged changes

View the difference between the last commit and staged changes:

```bash
git diff --staged
```

This helps verify what will be included in the next commit.

## Remove file from staging area

Remove a file from the staging area without deleting the file:

```bash
git restore --staged 06-staging-area.md
```

The file remains in the working directory, but it is no longer staged.

## Common commands

| Command                         | Description                                 |
| ------------------------------- | ------------------------------------------- |
| `git status`                    | Shows staged and unstaged changes           |
| `git add filename`              | Stages a specific file                      |
| `git add .`                     | Stages all changes in the current directory |
| `git diff`                      | Shows unstaged changes                      |
| `git diff --staged`             | Shows staged changes                        |
| `git restore --staged filename` | Removes a file from the staging area        |

## Example workflow

Check current status:

```bash
git status
```

Stage one file:

```bash
git add 06-staging-area.md
```

Check staged status:

```bash
git status
```

Review staged changes:

```bash
git diff --staged
```

Commit the staged file:

```bash
git commit -m "Add staging area notes"
```

## Browser workflow

When using GitHub browser, staging is mostly hidden.

In the browser, editing a file and selecting `Commit changes` usually creates a commit directly.

Basic browser workflow:

```text
Open file
Edit file
Preview changes
Commit changes
```

This is convenient for documentation, but it does not clearly show the staging area. Command-line Git gives better visibility and control.

## Troubleshooting

| Issue                          | Cause                          | Fix                                             |
| ------------------------------ | ------------------------------ | ----------------------------------------------- |
| File is not included in commit | File was not staged            | Use `git add filename`                          |
| Too many files are staged      | `git add .` staged extra files | Use `git restore --staged filename`             |
| Nothing to commit              | No files are staged            | Use `git add` before committing                 |
| Wrong file is staged           | Incorrect file was added       | Remove it using `git restore --staged filename` |
| Staged changes are unclear     | Changes were not reviewed      | Use `git diff --staged`                         |

## Notes

* The staging area prepares changes before commit.
* `git add` does not save changes permanently.
* A commit saves only staged changes.
* `git status` should be checked before every commit.
* Use `git add filename` when committing specific files.
* Use `git add .` only when all changes are related.
