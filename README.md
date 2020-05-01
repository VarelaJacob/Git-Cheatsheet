
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
* [Undoing Changes](#undoing-changes)
* [Rewriting git history](#rewriting-git-history)
* [Create a new repository](#create-a-new-repository)
* [Push an existing Git repository](#push-an-existing-git-repository)
* [Acknowledgements](#acknowledgements)

## Basic Commands
* git init
    * Creates a new Git repository in specified directory.
    * Run with no arguments to initialize the current directory as a git repository. 
* git clone <repo>
    * Clone repository at <repo> onto local machine. Original repository can be located on the local filesystem or on a remote machine via HTTP or SSH.
* git status
    * Inspects the contents of the working directory and staging area
* git add
    * Shows the difference between the working directory and the staging area
* git diff
    * Shows the difference between the working directory and the staging area
* git commit
    * Permanently stores file changes from the staging area in the repository
* git commit -m <message>
    * Commit the staged snapshot, uses <message> as the commit message. 
* git log
    * Shows a list of all previous commits.
* git checkout HEAD filename
    * Discards changes in the working directory
* git reset HEAD filename
    * Unstages file changes in the staging area
* git reset commit_SHA
    * Resets to a previous commit in your commit history 

### Git config
* git config --global user.name <name> 
    * Define the author name to be used for all commits by the current user.
* git config --global user.email <email>
    * Define the author email to be used for all commits by the current user.
* git config --global alias. <alias-name> <git-command>
    * Create a shortcut for a git command.
    * Example: alias.glog “log --graph
--oneline” will set ”git glog” equivalent to ”git log --graph --oneline.
* git config --system core.editor <editor> 
    * Set text editor used by commands for all users on the machine.
    * <editor> argument should be the command that launches the desired editor.
* git config --global --edit
    * Open the global configuration file in a text editor for manual editing. 

### Undoing Changes
* git revert <commit>
    * Create a new commit that undoes all of the changes made in <commit>, then apply it to the current branch.
* git reset <file> 
    * Remove <file> from the staging area, but leave the working directory unchanged. This unstages a file without overwriting any changes. 
* git clean -n
    * Shows which files would be removed from working directory.
    * Use the -f flag in place of the -n flag to execute the clean. 

### Rewriting git history
* 'git commit --amend'
    * Replace the last commit with the staged changes and last commit combined. 
    * Use with nothing staged to edit the last commit's message.
* `git rebase <base>`
    * Rebase the current branch onto <base>. 
    * <base> can be a commit ID, branch name, a tag, or a relative reference to HEAD.

## Create a new repository
* git clone https://github.com/VarelaJacob/Git-Cheatsheet.git
* cd Git-Cheatsheet.git
* touch README.md
* git add README.md
* git commit -m "add README"
* git push -u origin master

## Push an existing Git repository
* cd existing_repository
* git remote rename origin old-origin
* git remote add origin https://github.com/VarelaJacob/Git-Cheatsheet.git
* git push -u origin -all
* git push -u origin --tags

## Acknowledgements
* [Atlassian](https://www.atlassian.com/git)