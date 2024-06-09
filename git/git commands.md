# Getting & Creating Projects

If you are starting a repository locally and want to upload it to GitHub:

1. **Initialize the repository**:
   ```sh
   git init
   ```

2. **Add files to the staging area**:
   ```sh
   git add .
   ```

3. **Commit the changes**:
   ```sh
   git commit -m "Initial commit"
   ```

4. **Create a new repository on GitHub**:
   - Go to GitHub and create a new repository.

5. **Add the remote repository link**:
   ```sh
   git remote add origin <link>
   ```

6. **Verify the remote repository**:
   ```sh
   git remote -v
   ```

7. **Push the changes to GitHub**:
   ```sh
   git push -u origin main
   ```

To clone an existing repository:
```sh
git clone ssh://git@github.com/[username]/[repository-name].git
```

# Configuring Git

Set up your Git configuration:

1. **Set your username**:
   ```sh
   git config --global user.name "username"
   ```

2. **Set your email**:
   ```sh
   git config --global user.email "useremail"
   ```

3. **List all configurations**:
   ```sh
   git config --list
   ```

# Basic Snapshotting

## Staging Area
The staging area is where you can prepare changes before committing them. You can choose which changes to include in the next commit by adding them to the staging area.

## Commit
A commit is a snapshot of your project at a specific point in time, including the changes you've staged. Commits are permanent snapshots in the repository's history.

### Commands:

- **Check the status of your files**:
  ```sh
  git status
  ```

- **Add a specific file to the staging area**:
  ```sh
  git add [file-name.txt]
  ```

- **Add all new and changed files to the staging area**:
  ```sh
  git add -A
  ```
  or
  ```sh
  git add --all
  ```

- **Commit changes**:
  ```sh
  git commit -m "[commit message]"
  ```

- **Remove a file or directory from both the working directory and the Git repository**:
  ```sh
  git rm -r [file-name.txt]
  ```

- **Reset changes**:
  ```sh
  git reset [options] [<commit>]
  ```
  - Options:
    - `--mixed`: Move changes from the staging area back to the working directory (default).
    - `--soft`: Reset the commit history but keep changes in the staging area and working directory.
    - `--hard`: Reset the commit history and discard all changes in the staging area and working directory.

## Undoing Changes

### Staged Changes
- **Unstage specific changes**:
  ```sh
  git reset [filename]
  ```

- **Unstage all changes**:
  ```sh
  git reset
  ```

### Commits
- **Reset HEAD to one commit before**:
  ```sh
  git reset HEAD~1
  ```

- **Reset to a specific commit**:
  ```sh
  git log
  ```
  (Find the commit hash you want to reset to, then:)
  ```sh
  git reset [commit hash]
  ```

- **Hard reset to a specific commit**:
  ```sh
  git reset --hard [commit hash]
  ```

# Branching & Merging

## Branch
A branch is a separate workspace where you can make changes to your code without affecting the main codebase.

### Commands:

- **List branches** (the asterisk denotes the current branch):
  ```sh
  git branch
  ```

- **List all branches (local and remote)**:
  ```sh
  git branch -a
  ```

- **Create a new branch**:
  ```sh
  git branch [branch name]
  ```

- **Delete a branch**:
  ```sh
  git branch -d [branch name]
  ```

- **Delete a remote branch**:
  ```sh
  git push origin --delete [branch name]
  ```

- **Set up an upstream branch**:
  ```sh
  git push -u origin main
  ```

- **Create a new branch and switch to it**:
  ```sh
  git checkout -b [branch name]
  ```

- **Clone a remote branch and switch to it**:
  ```sh
  git checkout -b [branch name] origin/[branch name]
  ```

- **Rename a local branch**:
  ```sh
  git branch -m [old branch name] [new branch name]
  ```

- **Rename the current branch to a new name**:
  ```sh
  git branch -M [new branch name]
  ```

- **Switch to a branch**:
  ```sh
  git checkout [branch name]
  ```

- **Switch to the branch last checked out**:
  ```sh
  git checkout -
  ```

- **Discard changes to a file**:
  ```sh
  git checkout -- [file-name.txt]
  ```

- **Merge a branch into the active branch**:
  ```sh
  git merge [branch name]
  ```

- **Merge a branch into a target branch**:
  ```sh
  git merge [source branch] [target branch]
  ```

## Stashing
Stashing allows you to save changes in the working directory without committing them.

### Commands:

- **Stash changes in a dirty working directory**:
  ```sh
  git stash
  ```

- **Pop the most recent stash and apply it to the working directory**:
  ```sh
  git stash pop
  ```

- **List stashes**:
  ```sh
  git stash list
  ```

- **Apply a specific stash**:
  ```sh
  git stash apply <stash id>
  ```

- **Clear all stashes**:
  ```sh
  git stash clear
  ```

- **Save a stash with a message**:
  ```sh
  git stash save "message"
  ```

- **Create a branch from a stash**:
  ```sh
  git stash branch newbranch stash@{0}
  ```

# Sharing & Updating Projects

### Commands:

- **Push a branch to your remote repository**:
  ```sh
  git push origin [branch name]
  ```

- **Push changes to a remote repository and set the upstream branch**:
  ```sh
  git push -u origin [branch name]
  ```

- **Push changes to the remote repository (remembered branch)**:
  ```sh
  git push
  ```

- **Delete a remote branch**:
  ```sh
  git push origin --delete [branch name]
  ```

- **Update the local repository to the newest commit**:
  ```sh
  git pull
  ```

- **Pull changes from the remote repository**:
  ```sh
  git pull origin [branch name]
  ```

# Inspection & Comparison

### Commands:

- **View changes**:
  ```sh
  git log
  ```

- **View detailed changes**:
  ```sh
  git log --summary
  ```

- **View changes briefly**:
  ```sh
  git log --oneline
  ```

- **Preview changes before merging**:
  ```sh
  git diff [source branch] [target branch]
  ```

# Squashing Commits

Combining multiple commits into one:

1. **Reset to a specific commit**:
   ```sh
   git reset [commit hash]
   ```

2. **Rebase interactively**:
   ```sh
   git rebase -i [commit hash]
   ```
   - You can either `pick` or `squash` (`s`), merging commits into the previous one.
   - To save and exit, use `esc + : + wq`.

---

This should provide a clear, detailed, and well-organized overview of Git commands and concepts.