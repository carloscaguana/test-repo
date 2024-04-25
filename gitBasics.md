# Git Basics

This file contains information that I find important in order to understand and familiarize myself with Git. It includes commands, features, and additional information that makes it easy for me to reference as I progress.

NTS: **Create a Table of Contents**

## Git Setup

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

## Getting a Git Repository
There are 2 ways of getting a Git repository:

1. You can take a local directory that isn't under version control and turn it into a Git repository
2. You can clone an existing Git repository from Github onto your local device

### Option 1: Initializing a Repository in an Existing Directory
If you have an existing directory that isn't under version control, you can do so by first moving to that directory.

For MacOS:
`$ cd /Users/user/my_project`

For Windows: 
`$ cd C:/Users/user/my_project`

Once you find yourself in the desired directory, you want to type the following command:

`$ git init`

The command *init* is short for <u>initialize</u>. This creates a subirectory named `.git` which contains all repository files necessary to create a Git repository skeleton. It is important to note that at this point, nothing in the directory is tracked yet. 

### Option 2: Cloning an Existing Repository
To get a copy of a Git repository that already exists on GitHub, you simply use the command:


`git clone <url>`

To find the URL of the repository you want to clone:
1. Log in to GitHub.com
2. Find the repository you want to clone
3. Press on the green button that says 'Code'
4. Copy the HTTPS web URL
5. Paste the web URL into the terminal

NTS:**insert image of how to access repo url from GitHub**

The information in the URL would look something like this:

`https://github.com/username/repository-name`

When you create this clone on your local device, it creates a directory named `repository-name`, initializes a `.git` subdirectory inside it, pulls all the data from the repository, and checks out a working copy of the latest version.

You can also clone the repository into a directory with a different name:

`git clone <url> new-filename`


## Recording Files to the Repository
Each file in your working directory can be in one of two states: tracked or untracked. Tracked files are files that Git knows about while untracked files are files that Git is unaware of. 

![status of files](Images/fileStatus.png)

### Checking the Status of your Files
To check the status of the files in your working directory, you can use the following command:

`git status`

This command tells the user what branch they are one (usually *'main'*), as well as the state of the files in that working directory.

### Tracking New Files

To begin tracking a new file, you can use this command:

`git add <filename>`

This means that the file is tracked and staged, ready to be commited.

### Staging Modified Files
To stage a file that is unstaged, you simply use the `git add` command. This multipurpose command can be used to track new files and stage files.

Suppose you've already staged a file and you are ready to commit. However, you remember a small detail in that file that you want to change so you do so. If you were to run the `git status` command after that minor change, you would see that the file appears both as staged and unstaged.

This is because when you modified the file after staging it, the changes made to the file are unstaged. You would have to run the `git add` command again in order to stage the latest version of the file you're working on.

### Short Status

To see your changes in a more simplified way, you can simply run the following command:

`git status -s` or `git status --short`

`??`: means the file is not being tracked

`A`: the file has been added to the staging area

`M`: the file has been modified

### Ignoring Files

There are certain files you want to keep hidden, like log files or files created by your OS. You can add them to a `.gitignore` file so that these files aren't commited to the Git repository.

`#` functions like the `//` in Java. The line is not read and acts like a line to write comments.

### Viewing Your Staged and Unstaged Changes
If you want to know exactly what was changed in a file, you can use the command: 

`git diff`

It tells you the changes you've made that you havent staged yet. This command will give you no output if you've staged your changes.

`git diff --staged`
`git diff --cached`

This command compares your staged changes to your last commit. Use this command to see what you've staged that will go into your next commit.

---
### How to push an existing repository from git bash

`git remote add origin [https filepath]`

`git branch -M main`

`git push -u origin main`

`ls -al`