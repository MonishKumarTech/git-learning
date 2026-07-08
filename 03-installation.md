# Installation

## Overview

Git must be installed before using Git commands.

After installation, Git should be configured with a username and email address. This information is used in commit history.

## Key concepts

| Term                 | Description                                                   |
| -------------------- | ------------------------------------------------------------- |
| Git                  | Version control system used to track changes                  |
| Git Bash             | Command-line tool for using Git on Windows                    |
| Configuration        | Settings used by Git                                          |
| Global configuration | Git settings applied to all repositories for the current user |
| Commit identity      | The username and email stored with commits                    |

## Check Git installation

Check whether Git is installed:

```bash
git --version
```

Expected output format:

```text
git version 2.x.x
```

If the command returns a version number, Git is installed.

## Configure Git username

Set the username:

```bash
git config --global user.name "Your Name"
```

Example:

```bash
git config --global user.name "Hari Prasad"
```

## Configure Git email

Set the email address:

```bash
git config --global user.email "your-email@example.com"
```

Example:

```bash
git config --global user.email "hari@example.com"
```

Use the same email address connected to the GitHub account when possible.

## View Git configuration

View all global Git settings:

```bash
git config --global --list
```

Expected output:

```text
user.name=Hari Prasad
user.email=hari@example.com
```

## Common commands

| Command                                  | Description                      |
| ---------------------------------------- | -------------------------------- |
| `git --version`                          | Checks the installed Git version |
| `git config --global user.name "Name"`   | Sets the Git username            |
| `git config --global user.email "email"` | Sets the Git email address       |
| `git config --global --list`             | Shows global Git configuration   |

## Example workflow

Check Git version:

```bash
git --version
```

Set username:

```bash
git config --global user.name "Hari Prasad"
```

Set email:

```bash
git config --global user.email "hari@example.com"
```

Verify configuration:

```bash
git config --global --list
```

## Troubleshooting

| Issue                                      | Cause                                            | Fix                               |
| ------------------------------------------ | ------------------------------------------------ | --------------------------------- |
| `git` command not found                    | Git is not installed or not added to system path | Install Git and reopen terminal   |
| Wrong username in commits                  | Incorrect Git configuration                      | Update `user.name`                |
| Wrong email in commits                     | Incorrect Git configuration                      | Update `user.email`               |
| GitHub does not show commits under profile | Commit email may not match GitHub email          | Use the email connected to GitHub |

## Notes

* Git should be configured before creating commits.
* The username and email become part of commit history.
* `--global` applies the setting to all repositories for the current user.
* Git configuration can be checked using `git config --global --list`.
