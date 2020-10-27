# Init git repo

## 1. Init git
    git init

## 2. User name/email config

    git config --global user.name " "
    git config --global user.email " "

## 3. Connect to github
1. generate ssh key

        ssh-keygen -t rsa -C "your_email@example.com"

2. display ssh key

        cat /Users/xxx/.ssh/id_rsa.pub

3. link  

        git remote add origin "https:// ... .git"