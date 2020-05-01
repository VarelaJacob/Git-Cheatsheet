
<!-- PROJECT LOGO -->
<br />
<p align="center">
 <img src="images/Git-Logo.png" alt="Logo" width="80" height="80">


  <h3 align="center">Git Commands Cheatsheet</h3>

  <p align="center">
    This cheatsheet combines git commands from a variety of sources for quick and easy reference.
    <br />
    <br />
  </p>
</p>


## Table of Contents

* [Basic Commands](#basic-commands)
* [Git config](#git-config)
* [Git Push](#git-push)
* [Git Log](#git-log)
* [Undoing Changes](#undoing-changes)
* [Rewriting git history](#rewriting-git-history)
* [Git Branches](#git-branches)
* [Remote Repositories](#remote-repositories)
* [Git Rebase](#git-rebase)
* [Create a new repository](#create-a-new-repository)
* [Push an existing Git repository](#push-an-existing-git-repository)
* [Acknowledgements](#acknowledgements)

## Basic Commands
* `git init`
    * Creates a new Git repository in specified directory.
    * Run with no arguments to initialize the current directory as a git repository. 
* `git clone <repo>`
    * Clone repository at <repo> onto local machine. Original repository can be located on the local filesystem or on a remote machine via HTTP or SSH.
* `git status`
    * Inspects the contents of the working directory and staging area.
* `git add`
    * Shows the difference between the working directory and the staging area.
* `git diff`
    * Shows the difference between the working directory and the staging area.
* `git diff HEAD`
    - Show difference between working directory and last commit.
* `git diff --cached`
    * Show difference between staged changes and last commit. 
* `git commit`
    * Permanently stores file changes from the staging area in the repository.
* `git commit -m <message>`
    * Commit the staged snapshot, uses <message> as the commit message. 
* `git log`
    * Shows a list of all previous commits.
* `git rm <file>`
    * Delete the file from the project and stage the removal for commit. 
* `git mv <existing-path> <new-path>`
    * Change an existing file path and stage the move. 
* `git checkout HEAD filename`
    * Discards changes in the working directory.
* `git reset HEAD filename`
    * Unstages file changes in the staging area.
* `git reset commit_SHA`
    * Resets to a previous commit in your commit history.

## Git config
* `git config --global user.name <name>`
    * Define the author name to be used for all commits by the current user.
* `git config --global user.email <email>`
    * Define the author email to be used for all commits by the current user.
* `git config --global alias. <alias-name> <git-command>`
    * Create a shortcut for a git command.
    * Example: alias.glog “log --graph
--oneline”` will set ”git glog” equivalent to ”git log --graph --oneline.
* `git config --system core.editor <editor> `
    * Set text editor used by commands for all users on the machine.
    * <editor> argument should be the command that launches the desired editor.
* `git config --global --edit`
    * Open the global configuration file in a text editor for manual editing. 

## Git Push
* `git push <remote> --force`
    * Forces the git push even if it results in a non-fast-forward merge.
    * Do not use the `--force` flag unless you are absolutely sure you know what you are doing.
* `git push <remote> -all`
    * Push all of your local branches to the specified remote.
* `git push <remote> --tags`
    * Tags aren't automatically pushed when you push a branch or use the `--all` flag. The `--tags` flag sends all of your local tags to the remote repo.

## Git Log
* `git log -<limit>`
    * Limit number of commits by <limit>.
    * Example: `git -log -5` will limit to 5 commits.
* `git log --oneline`
    * Condense each commit to a single line.
* `git log -p`
    * Display the full diff of each commit.
* `git log --stat`
    * Include which files were altered and the relative number of lines that were added or deleted from each of them.
* `git log --author="<pattern>"`
    * Search for commits by a particular author.
* `git log --grep="<pattern>"`
    * Search for commits with a commit message that matches <pattern>
* `git log --stat -M`
    * Show all commit logs with indication of any paths that moved.
* `git log <since>..<until>`
    * Show commits that occur between <since> and <until>.
    * Arguments can be a commit ID, branch name, HEAD, or any other kind of revision reference.
* `git log -- <file>`
    * Only display commits that have the specified file.
* `git log --graph --decorate`
    * The `--graph` draws a text based graph of commits on the left side of commit messages. The `--decorate` flag adds names of branches or tags of commits shown.

## Undoing Changes
* `git revert <commit>`
    * Create a new commit that undoes all of the changes made in <commit>, then apply it to the current branch.
* `git reset <file> `
    * Remove <file> from the staging area, but leave the working directory unchanged. This unstages a file without overwriting any changes. 
* `git clean -n`
    * Shows which files would be removed from working directory.
    * Use the `-f` flag in place of the `-n` flag to execute the clean. 

## Rewriting git history
* `git commit --amend`
    * Replace the last commit with the staged changes and last commit combined. 
    * Use with nothing staged to edit the last commit's message.
* `git rebase <base>`
    * Rebase the current branch onto <base>. 
    * <base> can be a commit ID, branch name, a tag, or a relative reference to HEAD.
* `git reflog`
    * Show a log of changes to the local repository's HEAD.
    * add `--relative-date` flag to show date information.
    * Add `-all` flag to show all refs.

## Git Branches
* `git branch`
    * List all of the branches in your repo.
    * Add a <branch> argument to create a new branch with the name <branch>.
* `git checkout -b <branch>`
    * Create and check out a new branch named <branch>.
    * Drop the `-b` flag to checkout an existing branch.
* `git merge <branch> `
    * Merge <branch> into the current branch.

## Remote Repositories
* `git remote add <name> <url>`
    * Create a new connection to a remote repo.
    * After adding a remote, you can use <name> as a shortcut for <url> in other commands. 
* `git fetch <remote> <branch>`
    * Fetches a specific <branch>, from the repo.
    * Leave off <branch> to fetch all remote refs.
* `git pull <remote>`
    * Fetch the specified remote's copy of current branch and immediately merge it into the local copy.
* `git push <remote> <branch>`
    * Push the branch to <remote>, along with the necessary commits and objects. 
    * Creates named branch in the remote repo if it doesn't exist.
* `git pull --rebase <remote>`
    * Fetch the remote's copy of the current branch and rebases it into the local copy. Uses git rebase instead of merge to integrate the branches. 

## Git Rebase
* `git rebase -i <base>`
    * Interactively rebase current branch onto <base>. Launches editor to enter commands for how each commit will be transferred to the new base. 


## Create a new repository
* `git clone https://github.com/VarelaJacob/Git-Cheatsheet.git`
* `cd Git-Cheatsheet.git`
* `touch README.md`
* `git add README.md`
* `git commit -m "add README"`
* `git push -u origin master`

## Push an existing Git repository
* `cd existing_repository`
* `git remote rename origin old-origin`
* `git remote add origin https://github.com/VarelaJacob/Git-Cheatsheet.git`
* `git push -u origin -all`
* `git push -u origin --tags`

## Acknowledgements
* [Atlassian](https://www.atlassian.com/git)
* [Git-Tower](https://www.git-tower.com/blog/git-cheat-sheet/)
* [GitHub](https://education.github.com/git-cheat-sheet-education.pdf)