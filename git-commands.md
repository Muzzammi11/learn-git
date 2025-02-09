# Git Commands Reference Guide

## Basic Commands

| Command | Description |
|---------|-------------|
| `touch README.md` | Creates an empty `README.md` file |
| `git init` | Initializes a new Git repository in the current folder |
| `git status` | Shows the current status of the working directory (tracked/untracked files, changes, etc.) |
| `git add <filename>` | Stages a specific file for commit |
| `git add .` | Stages all modified and untracked files for commit |
| `git commit -m "commit message"` | Saves the staged changes with a message |
| `git commit --amend -m "new commit message"` | Modifies the last commit message |

## Configuration Commands

| Command | Description |
|---------|-------------|
| `git config --global user.email "your-email@example.com"` | Sets the global email for Git commits |
| `git config --global --list` | Displays the current global Git configuration |

## Remote Repository Commands

| Command | Description |
|---------|-------------|
| `git remote add origin <repository-url>` | Links the local repository to a remote GitHub repository |
| `git remote -v` | Displays the remote repository URLs for fetch and push operations |
| `git push -u origin main` | Pushes the local code to the `main` branch of the GitHub repository |

## Understanding Remote Operations

### Fetch and Push
- **Fetch**: Downloads data from the remote repository without merging
  ```bash
  git fetch origin
  ```
- **Push**: Uploads local commits to GitHub
  ```bash
  git push origin main
  ```

## Advanced Operations

### Deleting Commits from GitHub
```bash
# Undo the last commit
git reset --hard HEAD~1

# Update GitHub with the change
git push origin main --force
```


## Best Practices

1. Always write clear, descriptive commit messages
2. Commit frequently but meaningfully
3. Pull before pushing to avoid conflicts
4. Use branches for new features or bug fixes
5. Don't commit sensitive information or large binary files