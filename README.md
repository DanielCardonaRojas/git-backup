# git-backup

This project provides scripts and shell completions for backing up and restoring Git branches using Git bundle files.
It is designed to work with `zsh`.

## Features

- **Backup current branch to a bundle file**: Easily create backup bundle files for the current branch.
- **Restore branches from bundle files**: Restore branches from previously created bundle files.
- **Zsh completions**: Provides tab completion for bundle files during restore operations.

## Installation

1. **Clone the Repository**

```sh
git -C ~/.local/bin/ clone https://github.com/DanielCardonaRojas/git-backup.git
```

2. **Set Up Zsh Completions**

Create a completion script for zsh:

```sh
# Add the zsh completion file in one of the following locations:
echo $fpath
# Or source in your .zshrc
```

## Usage

**Backup you current branch**

```sh
git backup save
```

This will create a bundle file with a timestamp in the backup directory (/tmp/repo_backups/YOUR_REPO/YOUR_BRANCH).

**Restore a branch**

```sh
# Tab for suggestions on current available bundle files.
git backup restore <bundle_file>
```

