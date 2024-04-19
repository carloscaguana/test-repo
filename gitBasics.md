# Git Basics

This file contains information that I find important in order to understand and familiarize myself with Git. It includes commands, features, and additional information that makes it easy for me to reference as I progress.

## Git SetUp

`git config`

Lets you get and set configuration variables to customize your git environment

`git config user.name`

Displays the user's name/username

`git config user.email`

Displays the user's email

`git config --list`

Displays list of your configuration variables for git on your local system

`git config <key>`

Used to check a specific value for the given key

## Getting Help with Commands
There are 3 ways to get information from manual pages (manpage) while using Git:

`git <verb> -h`

`git help <verb>`

`git <verb> --help`

The first command will give you a short, concise version of the manpage that will appear in the Terminal (Mac) or in Git Bash (Windows). This command is good if you want to reference something real quick because you forgot.

The last two commands will give you a more extensive version of the manpage that includes even more information. If you're on Mac, this extensive version can be accessed through the Terminal. You can exit by pressing the 'Q' button. On Windows, it will open up a new window on your  browser with all the information.

NTS: **LEFT OFF ON PAGE 26**

---
### How to push an existing repository from git bash

`git remote add origin [https filepath]`

`git branch -M main`

`git push -u origin main`

`ls -al`