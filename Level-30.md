# Level 30
Current user: bandit29

## Concept - Git & Branches 🎯 
You're probably familiar with github and have seen that a repository can have multiple branches. This is exactly the concept here. We're not only dealing with the origin branch, but also with sub branches that have the password we're looking for.


## Commands - Three
git, git checkout, git branch -a

## Hint
Try reading the README.md file. Is the password visible? No. It is not in production. What branch represents production in git? Can we find if there are other branches?

## Solution
Make sure you have exited from bandit servers by running exit.

Execute:

 git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo

 Enter password which is same as bandit29: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0

 Then check directories on your machine using cd

 You should see repo. Run ls and you'll find README.md file.

 cat README.md

/# Bandit Notes
Some notes for level29 of bandit.

/## credentials

- username: bandit30
- password: <no passwords in production!>
 
This right here is the hint we need. No passwords in production...means no password in the main branch! But we have other branches don't we? Let's check:

git branch -a

Switch to dev branch using:

git checkout dev

You should get an output verifying that you switched to dev branch.

ls in this branch and you find README file. Read its contents using cat:

cat README.md

/# Bandit Notes
Some notes for bandit30 of bandit.

/## credentials

- username: bandit30
- password: jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX

And now you have the bandit30 password!

## Voila!🎉
