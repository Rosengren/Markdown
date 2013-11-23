#Git

Configure Git for the first time
---
After installing git, run the following commands:

    git config --global user.name "firstName lastName"
    git config --global user.email "email@address.com"

Create SSH key (see SSH Key) and add key to git server

Setup New Git Repo
---

To initialize git and add files to new repo run the commands:

    git init
    git status  # check current tacked files
    git add .   # add all files/folders
    git commit -m "initial commit" # commit & add message


Undo change using git:

    git add .
    git checkout -f

SSH Key
---
Create a new SSH Key:

    ssh-keygen -t rsa "your_email@example.com"

Most Used Commands
---

Push changes to online repository:

    git add .
    git commit -m "message"
    git push

Create New Repo
---
Create a new repository on the command line:

    touch README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin https://github.com/Rosengren/pinteresting.git
    git push -u origin master

Push an existing repository from the command line:

    git remote add origin https://github.com/Rosengren/pinteresting.git
    git push -u origin master