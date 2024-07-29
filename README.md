
# Git Cheat Sheet for DevOps Engineers

## Introduction to Git

Git is a distributed version control system designed to handle everything from small to very large projects with speed and efficiency. It allows multiple developers to work on a project simultaneously without overwriting each other's changes. Git tracks changes, allows you to revert to previous states, and collaborate with others seamlessly.

## Basic Git Commands

### 1. Git Configuration
Configure your Git environment with your user name and email.
```sh
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### 2. Initializing a Repository
Create a new Git repository.
```sh
git init
```

### 3. Cloning a Repository
Clone an existing repository.
```sh
git clone https://github.com/username/repository.git
```

### 4. Checking Repository Status
Check the status of your files in the working directory and staging area.
```sh
git status
```

### 5. Adding Files
Add files to the staging area.
```sh
git add filename
git add .
```

### 6. Committing Changes
Commit changes in the staging area to the repository.
```sh
git commit -m "Your commit message"
```

### 7. Viewing Commit History
View the commit history of the repository.
```sh
git log
```

### 8. Pushing Changes
Push changes to the remote repository.
```sh
git push origin branch_name
```

### 9. Pulling Changes
Fetch and merge changes from the remote repository to your local repository.
```sh
git pull origin branch_name
```

### 10. Creating a Branch
Create a new branch.
```sh
git branch branch_name
```

### 11. Switching Branches
Switch to another branch.
```sh
git checkout branch_name
```

### 12. Merging Branches
Merge a branch into the current branch.
```sh
git merge branch_name
```

### 13. Deleting a Branch
Delete a branch.
```sh
git branch -d branch_name
```

## Advanced Git Commands

### 14. Stashing Changes
Stash changes in the working directory.
```sh
git stash
```

### 15. Applying Stash
Apply stashed changes.
```sh
git stash apply
```

### 16. Creating Tags
Create a new tag.
```sh
git tag tag_name
```

### 17. Pushing Tags
Push tags to the remote repository.
```sh
git push origin tag_name
```

### 18. Resolving Merge Conflicts
When a merge conflict occurs, Git will pause the merge and allow you to resolve the conflicts manually. After resolving the conflicts, you need to mark them as resolved.
```sh
# After resolving conflicts in the files
git add filename
git commit -m "Resolved merge conflict"
```

### 19. Viewing Differences
View changes between commits, branches, etc.
```sh
git diff
```

### 20. Resetting Changes
Reset the current HEAD to the specified state.
```sh
git reset --hard commit_id
```

### 21. Reverting a Commit
Create a new commit that undoes the changes from a previous commit.
```sh
git revert commit_id
```

### 22. Rebasing
Rebase the current branch onto another branch.
```sh
git rebase branch_name
```

### 23. Cleaning Untracked Files
Remove untracked files from the working directory.
```sh
git clean -f
git clean -fd
```

### 24. Bisecting
Use binary search to find the commit that introduced a bug.
```sh
git bisect start
git bisect bad
git bisect good commit_id
```

### 25. Cherry-picking
Apply the changes introduced by some existing commits.
```sh
git cherry-pick commit_id
```

### 26. Git Hooks
Customize Git’s behavior by using scripts triggered by operations.
- `pre-commit`: Runs before a commit is made.
- `pre-push`: Runs before a push is made.
- `post-merge`: Runs after a merge is completed.
```sh
# Example: .git/hooks/pre-commit
#!/bin/sh
# Pre-commit hook script
```

### 27. Git Submodules
Include other repositories as subdirectories.
```sh
git submodule add https://github.com/username/repository.git
git submodule update --init --recursive
```

### 28. Checking out Remote Branches
Create a new local branch tracking a remote branch.
```sh
git checkout -b local_branch_name origin/remote_branch_name
```

### 29. Working with Remotes
Add, remove, and manage remote repositories.
```sh
git remote add origin https://github.com/username/repository.git
git remote -v
git remote rm origin
```

### 30. Fetching Changes
Fetch updates from the remote repository without merging.
```sh
git fetch origin
```

## Git Workflow

1. **Clone the repository**:
   ```sh
   git clone https://github.com/username/repository.git
   ```

2. **Create a new branch**:
   ```sh
   git checkout -b new_feature
   ```

3. **Make changes and commit**:
   ```sh
   git add .
   git commit -m "Implemented new feature"
   ```

4. **Push changes**:
   ```sh
   git push origin new_feature
   ```

5. **Create a Pull Request (PR)** on the remote repository to merge your changes into the main branch.

## Best Practices

- **Commit Often**: Commit your work frequently with meaningful commit messages.
- **Branching**: Use branches for each feature or bug fix to keep the main branch clean.
- **Pull Frequently**: Pull changes from the remote repository to stay updated with the latest code.
- **Resolve Conflicts Early**: Resolve merge conflicts as soon as they arise to avoid complications.
- **Use .gitignore**: Define a `.gitignore` file to exclude files that do not need to be versioned.

## Conclusion

Git is a powerful tool that, when used correctly, can greatly enhance your productivity and collaboration on software projects. This cheat sheet provides a quick reference to the most commonly used Git commands. For more detailed information, refer to the [official Git documentation](https://git-scm.com/doc).
