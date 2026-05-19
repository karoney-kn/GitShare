# Git-commands

## Git Start up
creat a repo on the git page

git config --global user.name "username"

git config --global user.email "email"

git config --list

## Generate SSH Key
first:

ssh-keygen -t ed25519 -C "your_email@example.com"

then:

cat ~/.ssh/id_ed25519.pub

add the key to new ssh key in github account 
## Fetches GitHub’s SSH key and adds it to your trusted list, bypassing the "authenticity can't be established" prompt.
then:

ssh-keyscan github.com >> ~/.ssh/known_hosts

## Test SSH Connection to check that the SSH connection works:
finally:

ssh -T git@github.com

## Cloning the repo
git clone git@github.com:user.name/userrepo.git

git init 

git status 

git add . 

git branch -M main

git commit -am "your comments"

git push -u origin main

## To pull changes done on the remote server
git pull
## File to Ignore from the repo 
create .gitignore file

## Create a branch
git branch branch-name
or
git checkout -b branch-name
## Delete a branch
git push origin --delete branch-name --> remote delete

git branch -d branch name --> for local delete

## To Merge the branch to main
first:

git checkout/switch main

then:

git merge branch-name

finally:

git push -u origin main

## Log Status
git log

git log --oneline

git log --all --graph

git remote set-url origin git@github.com:<username>/<repository_name>.git

git commit -am "your comments"

git push --set-upstream origin main

## Rebase match
git config pull.rebase true

git pull

