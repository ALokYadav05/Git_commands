# Git-Flow Commands :

## ----- Initial Setup & Project Start -----

1) `git config --global user.name "demo"`
* Sets your display name globally for every repository on your machine.

2) `git config --global user.email "demo@example.com"`
* Sets your email address globally; this info is attached to every commit you make.

3) `git init`
* Transforms the current directory into a Git repository by creating a hidden .git folder.

4) `git add .`
* Stages all changes (new, modified, or deleted files) in the current directory for the next commit.

5) `git commit -m "first commit"`
* Records the staged snapshot in the project history with a descriptive message.

6) `git branch -M main`
* Renames the default branch to main (modern standard).

7) `git remote add origin https://github.com...`
* Connects your local repository to a remote server (like GitHub).

## ----- Git Flow Workflow -----

8) `git flow init`
* Initializes the Git Flow extension, setting up naming conventions for main, develop, and feature branches.

9) `git branch`
* Lists all local branches in your repository and highlights the one you are currently on.

10) `git flow feature start feature1`
* Creates and switches to a new branch named feature/feature1, based on the develop branch.

11) `git flow feature finish feature1`
* Merges feature/feature1 back into develop, deletes the feature branch, and switches you back to develop.

12) `git push -u origin main`
* Uploads your local main branch to the remote and sets it as the upstream default.

13) `git push -u origin develop`
* Uploads and tracks your local develop branch on the remote server.

## ----- Releasing -----

14) `git flow release start 1.0.0`
* Starts a release branch to prepare for version 1.0.0 (used for final bug fixes and metadata).

15) `git flow release finish -m "Your message"`
* Finalizes the release by merging it into both main and develop, and tags it as 1.0.0.

Vim Tip: Press i for insert mode, Esc then :wq and Enter to save and exit.

16) `git push --tags`
* Pushes all local commits and specifically your release tags to the remote repository.

## ----- Managing Unfinished Work (Stashing) -----

17) `git stash`
* Temporarily "shelves" your uncommitted changes and resets your branch to a clean state.

18) `git stash list`
* Shows a list of all your saved stashes with their unique IDs (like stash@{0}).

19) `git stash pop`
* Re-applies the most recent stash to your current branch and deletes it from the stash list.

20) `git stash apply`
* Re-applies the stash but keeps it in the list for use on other branches.

## -----  Synchronizing with Remotes -----

21) `git remote -v`
* Lists all connected remote repositories and their URLs for fetching and pushing.

22) `git fetch`
* Downloads new data from the remote repository to your local machine without merging it.

23) `git pull`
* Fetches and immediately merges the latest remote changes into your current branch.

## -----  Integrating Changes -----

24) `git merge <branch-name>`
* Joins the history of another branch into your current one using a "merge commit."

25) `git rebase <branch-name>`
* Re-writes your commit history by moving your local commits to the tip of the target branch for a linear history.
* Warning: Never rebase branches that have already been pushed to a public repository.

## ----- Inspection & Undoing Changes -----

26) `git status -s`
* Gives a short, summarized version of the status of your modified files.

27) `git log --oneline --graph`
* Displays your commit history as a compact, visual tree diagram.

28) `git checkout <file_name>`
* Discards local changes to a specific file and restores it to the last committed state.

29) `git reset --hard HEAD`
* Completely wipes out all uncommitted changes and returns to the last commit (use with caution).
