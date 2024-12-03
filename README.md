# Git and GitHub Command Cheatsheet

## **Basic Setup**
- `git config --global user.name "Your Name"`: Set your Git username.
- `git config --global user.email "your.email@example.com"`: Set your Git email.
- `git config --list`: List all Git configurations.

---

## **Initializing and Cloning**
- `git init`: Initialize a new Git repository.
- `git clone <repo-url>`: Clone an existing repository.

---

## **Working with Changes**
- `git add <file>`: Stage a specific file for commit.
- `git add .`: Stage all changes in the current directory.
- `git commit -m "Commit message"`: Commit changes with a message.
- `git commit -am "Message"`: Add and commit tracked files in one step.
- `git commit --amend`: Edit the last commit message or add changes to it.

---

## **Status & Logs**
- `git status`: Show the current status of changes.
- `git log`: View commit history.
- `git log --oneline`: Show concise commit history.

---

## **Branching & Merging**
- `git branch <branch-name>`: Create a new branch.
- `git checkout <branch-name>`: Switch to a specific branch.
- `git checkout -b <branch-name>`: Create and switch to a new branch.
- `git merge <branch-name>`: Merge a branch into the current branch.
- `git rebase <branch-name>`: Reapply commits on top of another base.
- `git rebase -i HEAD~<n>`: Interactive rebase to edit commit history.
- `git branch -d <branch-name>`: Delete a local branch (use `-D` to force delete).

---

## **Handling Merge Conflicts**
- `git diff`: Compare working directory changes.
- `git diff <branch1> <branch2>`: Compare two branches.
- **Resolving conflicts**: Open files, fix conflicts, then add and commit.

---

## **Remote Repositories**
- `git remote add origin <url>`: Link your local repository to a remote one.
- `git remote -v`: List the remote repository URLs.
- `git remote set-url origin <new-url>`: Update the remote URL.
- `git remote rename <old-name> <new-name>`: Rename a remote.
- `git push -u origin <branch-name>`: Push changes to the remote repository.
- `git pull origin <branch-name>`: Pull changes from the remote branch.
- `git fetch`: Download updates from the remote without merging.
- `git fetch <remote>`: Fetch updates from a specific remote.

---

## **Undoing Changes**
- `git reset <file>`: Unstage a file.
- `git reset --soft HEAD~1`: Undo the last commit but keep changes staged.
- `git reset --mixed HEAD~1`: Undo the last commit, keep changes unstaged.
- `git reset --hard HEAD~1`: Completely remove the last commit.
- `git revert <commit-id>`: Create a new commit to undo a specific commit.

---

## **Stashing Changes**
- `git stash`: Temporarily save changes.
- `git stash list`: View stashed changes.
- `git stash pop`: Reapply stashed changes and remove them from the stash.
- `git stash apply`: Reapply stashed changes without removing them.
- `git stash clear`: Remove all stashed entries.

---

## **Advanced Operations**
- `git cherry-pick <commit-id>`: Apply a specific commit from another branch.
- `git cherry-pick <start-commit-id>^..<end-commit-id>`: Cherry-pick a range of commits.
- `git tag <tag-name>`: Add a tag to a commit.
- `git tag -d <tag-name>`: Remove a local tag.
- `git reflog`: View history of all changes.
- `git reflog show <branch-name>`: Show reflog for a specific branch.
- `git show <commit-id>`: Show detailed info for a specific commit.
- `git bisect start`: Start bisecting to locate a bug.

---

## **Collaborating & Pull Requests**
- `git branch -a`: List all branches, including remote branches.
- `git push origin :<branch-name>`: Delete a remote branch.
- **Creating a Pull Request**: Go to your GitHub repository, select your branch, and click “New Pull Request.”

---

## **Reviewing Changes**
- `git show <file>`: Display changes made to a specific file.
- `git diff <commit-id1> <commit-id2>`: Compare changes between two commits.

---

## **GitHub Commands (Optional with GitHub CLI)**
- `gh repo create`: Create a new GitHub repository from the command line.
- `gh repo clone <repo-url>`: Clone a GitHub repository.
- `gh pr create`: Create a pull request from the command line.
- `gh pr list`: List open pull requests in the repository.
- `gh issue create`: Create a GitHub issue from the command line.

---

## **Help Commands**
- `git help <command>`: Get detailed help for a specific command.

---

## **Submodules & Worktrees**
- `git submodule add <repo-url> <path>`: Add a submodule.
- `git submodule init`: Initialize submodules.
- `git submodule update`: Update submodules.
- `git worktree add <path> <branch>`: Create a new working tree for a branch.

---

## **Cleaning Up**
- `git clean -f`: Remove untracked files.
- `git clean -fd`: Remove untracked files and directories.
- `git gc --prune=now`: Clean up unnecessary files and optimize the repository.

---

## **Repository Management**
- `git shortlog -s -n`: Summarize commits by author.
- `git describe --tags`: Get a readable name for a commit.
- `git blame <file>`: Show who last modified each line of a file.
- `git grep "search-term"`: Search for a term in the repository.
- `git revert <commit-id1>..<commit-id2>`: Revert a range of commits.
- `git archive --format=zip HEAD -o latest.zip`: Archive the latest commit as a ZIP file.
- `git fsck`: Check the object database for integrity.
