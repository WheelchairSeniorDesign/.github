# How to use Git

## Git Setup

- Make sure git is installed on your machine
  - Can check with `git -v` from terminal
- Make sure you have a GitHub account and have access to project repos
- Create a local folder on your computer where you want to store your local project
- Use - within local folder (can add `--global` before `user.name` / `user.email`) to connect to GitHub account
  - `git config user.name "GitHub username"`
  - `git config user.email "GitHub email"`
- Within local folder - `git clone <repository link from github>`

## Basic Git Commands - Add, Commit, Push

- You can use your IDE with Git, but here are some basic commands
- `git add .` - Adds all the files in the current directory to git
- `git commit -m "Message"` - Commits changes to git with a commit message
- `git push` - Pushes your changes to it
- Helpful:
  - `git status` can show the current state of the local repo
  - `git restore <filename>` will revert a file to its last pulled state
- Note: You can use `git add/restore .` for all files or `git add/restore <filename>` for a single file

## Branching

- When you are working, create a new branch off of main so that your code doesn’t conflict with other people’s
- Use `git branch <branch name>` to create a new branch
- Helpful: Use `git branch` to view all branches and see which one you are on, or `git status` will show the current branch
- Use `git switch <branch name>` to switch branches
- Once you are on your branch, use your standard add, commit, and push commands to make changes
- **You should almost never push directly to main**, make sure you are working on a branch!

## Pull Requests

- Once you are done with your code and want to merge it into main, create a pull request to merge your branch into main.
- A pull request is made directly in GitHub and is a way to review and approve code before two branches are merged.
- Team members will review your code before approving it to merge into main.
- If you have merge conflicts, resolve them (use a GUI for this).
- Once you finish your pull request, delete your branch unless you have some reason to keep it around.

## Other Notes

- Good practice is to always pull before you start working (pull any updates to avoid merge conflicts down the road).
- Whatever code you push is seen by everyone else along with who pushed what specific files/lines.
- **PLEASE COMMENT YOUR CODE & KEEP IT CLEAN** - Others will not be able to review or help debug if your code is sloppy.
- Use `git restore` to help resolve merge conflicts.

## Git Commands

- `git -v`: Displays the version of Git installed on your machine.
- `git config user.name "GitHub Username"`: Sets the Git username for the current repository.
- `git config --global user.name "GitHub Username"`: Sets the Git username globally for all repositories.
- `git config user.email "GitHub Email"`: Sets the Git email for the current repository.
- `git config --global user.email "GitHub Email"`: Sets the Git email globally for all repositories.
- `git clone <repository link from github>`: Clones a repository from GitHub to your local machine.
- `git add .`: Adds all changes in the current directory to the staging area.
- `git add <filename>`: Adds a specific file to the staging area.
- `git commit -m "Push Message"`: Commits the staged changes with a commit message.
- `git push`: Pushes the committed changes to the remote repository.
- `git restore .`: Restores all files in the current directory to their last committed state.
- `git restore <filename>`: Restores a specific file to its last committed state.
- `git branch <branchname>`: Creates a new branch with the specified name.
- `git branch`: Lists all branches and shows the current branch.
- `git status`: Displays the state of the working directory and the staging area.
- `git checkout <branchname>` Checks out a branch (use switch instead since it is newer).
- `git switch <branchname>`: Switches to the specified branch.
- `git reset HEAD~1`: Resets the current branch to the previous commit, keeping changes in the working directory.
- `git tag`: Lists all tags in the repository.
- `git rebase`: Reapplies commits on top of another base tip.


# PCB Design in Git

- We will be using git to store KiCad files as well so that we can have a running record of them.
- Put all the PCBs in a subfolder in the PCB repo.
- Make a branch for your board, and only work on that board on the corresponding branch.
- Don’t delete your branch once you merge it; keep making changes on that branch.
- Only one person should work on a board at a time, and all changes should be committed before the next person works on it.


