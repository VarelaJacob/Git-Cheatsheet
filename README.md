
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



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Basic Commands](#basic-commands)
* [Git global setup](#git-global-setup)
* [Acknowledgements](#acknowledgements)
* [Create a new repository](#create-a-new-repository)
* [Push an existing Git repository](#push-an-existing-git-repository)

## Basic Commands
* git init
    * Creates a new Git repository
* git status
    * Inspects the contents of the working directory and staging area
* git add
    * Shows the difference between the working directory and the staging area
* git diff
    * Shows the difference between the working directory and the staging area
* git commit
    * Permanently stores file changes from the staging area in the repository
* git log
    * Shows a list of all previous commits.
* git checkout HEAD filename
    * Discards changes in the working directory
* git reset HEAD filename
    * Unstages file changes in the staging area
* git reset commit_SHA
    * Resets to a previous commit in your commit history 

## Git global setup
* git config --global user.name "FirstName LastName"
* git config --global user.email "email@address.com"

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

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [Img Shields](https://shields.io)

