# First repository

## Overview

A repository is a project folder tracked by Git.

A Git repository stores files, changes, and commit history. It can be created locally using Git commands or directly on GitHub.

For this repository, GitHub is used to store Markdown notes and track learning progress.

## Key concepts

| Term              | Description                                   |
| ----------------- | --------------------------------------------- |
| Repository        | A project folder tracked by Git               |
| Local repository  | A repository stored on the computer           |
| Remote repository | A repository stored online, such as on GitHub |
| `README.md`       | Main documentation file of a repository       |
| Commit            | A saved change in the repository history      |
| Main branch       | The default branch used for stable work       |

## Create a repository on GitHub

Use these settings when creating a repository on GitHub:

| Field            | Value                                                                                                                      |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Repository name  | `git-learning`                                                                                                             |
| Description      | Practical Git and GitHub notes, commands, workflows, and version control concepts for IT Support and System Administration |
| Visibility       | Public                                                                                                                     |
| Add `README.md`  | Yes                                                                                                                        |
| Add `.gitignore` | No                                                                                                                         |
| License          | No                                                                                                                         |

## Repository name

Use a short and clear repository name.

Good example:

```text
git-learning
```

Avoid unclear names:

```text
my-notes
git-final
practice-new
```

A clear name helps others understand the purpose of the repository.

## Repository description

Use a direct description.

```text
Practical Git and GitHub notes, commands, workflows, and version control concepts for IT Support and System Administration.
```

The description should explain what the repository contains.

## Create files in GitHub browser

To create a new file in GitHub:

1. Open the repository.
2. Select `Add file`.
3. Select `Create new file`.
4. Enter the filename.
5. Add the content.
6. Select `Commit changes`.

Example filenames:

```text
README.md
01-why-git-exists.md
02-git-architecture.md
03-installation.md
04-first-repository.md
```

## Create a repository using Git commands

Create a project folder:

```bash
mkdir git-learning
```

Enter the folder:

```bash
cd git-learning
```

Initialize Git:

```bash
git init
```

Rename the default branch to `main`:

```bash
git branch -M main
```

Check repository status:

```bash
git status
```

## Common commands

| Command              | Description                          |
| -------------------- | ------------------------------------ |
| `mkdir git-learning` | Creates a project folder             |
| `cd git-learning`    | Enters the project folder            |
| `git init`           | Initializes a Git repository         |
| `git branch -M main` | Renames the current branch to `main` |
| `git status`         | Shows the current repository status  |

## Example workflow

Create a repository folder:

```bash
mkdir git-learning
```

Move into the folder:

```bash
cd git-learning
```

Start Git tracking:

```bash
git init
```

Set the branch name:

```bash
git branch -M main
```

Check the result:

```bash
git status
```

Expected output:

```text
On branch main

No commits yet
```

## Browser workflow

When using GitHub browser, file creation and commits happen directly on GitHub.

Basic browser workflow:

```text
Create repository
Create file
Add content
Commit changes
View repository files
```

This workflow is useful for writing documentation, but command-line Git is still required for deeper Git practice.

## Troubleshooting

| Issue                          | Cause                                               | Fix                               |
| ------------------------------ | --------------------------------------------------- | --------------------------------- |
| Repository name already exists | Another repository has the same name in the account | Use a different clear name        |
| File is not visible            | File was not committed                              | Commit the file after creating it |
| Wrong file name                | Filename was typed incorrectly                      | Rename the file                   |
| Empty repository               | No file has been created or committed               | Add `README.md` or another file   |
| Wrong branch name              | Repository is using a different default branch      | Rename branch to `main` if needed |

## Notes

* A repository stores project files and Git history.
* `README.md` explains the purpose of the repository.
* GitHub browser can be used to create files and commits.
* Command-line Git gives better control over repository workflow.
* Repository names should be clear, short, and lowercase.
