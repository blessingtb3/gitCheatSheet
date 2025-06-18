**Git cheat sheet**

**Configuration**
git config --global user.name "Your Name" # Set the username for commits
git config --global user.email "your.email@example.com" # Set the email for commits


**Create a new repository**
git init # Initialise a new Git repository


**Clone a repository**
git clone <repository-url> # Clone an existing repository from a URL


**Check status**
git status # Show the working directory status


**Add changes**
git add <file> # Stage a specific file for commit
git add . # Stage all changes in the working directory


**Commit changes**
git commit -m "Commit message" # Commit staged changes with a message


**View commit history**
git log # Show the commit history


**Create a new branch**
git branch <branch-name> # Create a new branch


**Switch branches**
git checkout <branch-name> # Switch to a specified branch


**Merge branches**
git merge <branch-name> # Merge changes from the specified branch into the current branch


**Delete a branch**
git branch -d <branch-name> # Delete a specified branch


**Push changes to remote**
git push origin <branch-name> # Push local changes to the remote repository


**Pull changes from remote**
git pull origin <branch-name> # Fetch and merge changes from the remote repository


**Fetch changes from remote**
git fetch # Download changes from the remote repository without merging


**Stash changes**
git stash # Temporarily store changes that are not ready to be committed
git stash pop # Apply the stashed changes back to the working directory


**Show differences**
git diff # Show unstaged changes
git diff --staged # Show changes that are staged for the next commit


**Reset changes**
git reset <file> # Unstage a specific file
git reset --hard HEAD # Reset the working directory to the last commit, discarding all changes


**Tagging**
git tag <tag-name> # Create a tag for a specific commit
git push origin <tag-name> # Push the tag to the remote repository


**View remote repositories**
git remote -v # List remote repositories and their URLs


**Add a remote repository**
git remote add origin <repository-url> # Add a new remote repository


**Remove a remote repository**
git remote remove origin # Remove an existing remote repository


### Rebasing Main on Your Branch

1. On your branch, execute:
   ```bash
   git rebase -i HEAD~4
   ```
   Replace `4` with the number of commits you have on your branch.

2. When the text editor opens, press `i` to enter insert mode. 

3. Leave `pick` for the first commit message and change `pick` to `s` for all subsequent commit messages.

4. Once you have made the changes, press `Esc`, then type `:wq` and hit `Enter` to save and exit.

5. In the next text file that opens, press `i` and prepend `#` to the start of all commit messages except for the first one.

6. After you've made these changes, press `Esc`, then type `:wq` and hit `Enter` to save and exit.

7. Push your changes with:
   ```bash
   git push origin my-branch-name --no-verify --force
   ```

8. Switch to the main branch:
   ```bash
   git checkout main
   ```

9. Update your local main branch:
   ```bash
   git pull
   ```

10. Switch back to your branch:
    ```bash
    git checkout my-branch-name
    ```

11. Rebase your branch onto main:
    ```bash
    git rebase main
    ```

12. Resolve any merge conflicts using VSCode's merge editor, and click "Complete Merge" after each change.

13. Continue the rebase process:
    ```bash
    git rebase --continue
    ```

You’re all set!






[notes on conventional commits and branch naming]: https://dev.to/varbsan/a-simplified-convention-for-naming-branches-and-commits-in-git-il4
**This cheat sheet has been created by Blessing Baloyi with the help of ZebraGPT**
