Git SheetCheat

A Version Control Software

Git Configuration Levels

System: 

Apply to all users of a computer

storage location: 

-Windows:

Program

Files\Git\etc\gitconfig

Linux-Mac



User: 

-Apply to a single user and all the projects that the user works on

-Stored inside the user's home directory

Stored inside a file called .gitconfig

&nbsp;

Projects:

Unique to each project

Stored inside the project directory inside a directory called .git with a file called config.

Project settings will override any of the system or user configurations if they're different



Set Git Configuration Command

System

>git config --system

User

>git config --global

Project

>git config



Important User Configurations

Programmer Name and email: 

>git config --global user.name "Your Name"

>git config --global user.email "your\_email@sever.com"

Default Branch 

>git config --global init.defaultBranch main



How Does Git Work?

Git records snapshots of a programmer's work, on commit it takes a picture of what all the files look like, and if the files aren't changed it saves a link to the file that's already stored



Files States

Files in Git can have three states

-Modified:The file has been changed but not yet committed to the local database

-Staged: Meaning that a file has been marked in its current version to go into the next commit(version)

-Committed/Unmodified: The data is safely stored in the local database or repository



Sections of a Git Project

-Working Area

-Staging Area

-Git Directory



Git Help

>git help command: will open the file for the command and give descriptions and more



Git Messages

Give detailed and relevant commit messages



Update a Commit

git commit --amend

allows the user to modify the last commit instead of creating a new one



File Changes in the Repo

Operating systems use the file path with the file name to locate a file, so if a file is renamed the file path changes. Renaming is recognized as moving to the system.



remove file or rename: git rm file\_Name

git add new\_file\_Name

or both commands can be done at once with: git mv file\_Name new\_file\_Name



Working with Remote Repos

-Push: upload changes to remote repo

-Pull: pull changes from remote repo to local to get an updated version of the project

-Pull Request: tell others about the changes to pull from local to remote



Important Commands and Terminology



Repository: A place where you can store your code, your files, and each file's revision history

Branch: Each Repository has one default branch. Branch used to isolate development work without affecting other branches in the repository



Local Repo: Local repositories reside on the computers of team members

Remote Repo: hosted on a server that is accessible to all team members(ex: GitHub)

Commit: snapshot or checkpoint

Clone: copying from local or remote repo

Push: upload local changes to remote repo

Pull: Pull changes from the remote repo to your local(to get an updated version of the project)

Pull Request: tell others about your changes to pull from local to remote

Note: Anyone can push and pull depends on permission(before a modification is pushed it must be revised and approved)



Git Commands

git help

git init <directory> initializes an empty repository

git clone <repository> Copy an existing repository from a remote location with all its info

git add <file> Stages a file to prepare it for a commit. Staging saves the current state of the file- modifying a file after add it will lead to two states of the file

git commit -m <message>: Create a commit object, a new version

git status: Displays the states of files

git diff <file>: Shows what you changed exactly

git log: What were the last couple of commits

git rm <file>: Removes a file from tracked files and working directory and needs to commit after



