# Level 29
Current user: bandit28

## Concept - Git & Git Logs 🎯 
Git is an open source that allows for sharing repositories (repos) between machines securely and efficiently. We're going to learn how to use git along with ssh.

We all change our repositories multiple times. Sometimes we need to cover important data, other times we need to fix a branch etc...
But if we were able to view the history of what we did? Turns out Git offers command to view history of commits and the version of files at these commits (before they were done) 😉.


## Commands - Three
git, git log, git show

## Hint
Try reading the README.md file. Is the password visible? Is there a way to view the password before they changed it to xxxxx? Browse for git log and git show to see how they are used

## Solution
Make sure you have exited from bandit servers by running exit.

Execute:

 git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo

 Enter password which is same as bandit28: y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ

 Then check directories on your machine using cd

 You should see repo. Run ls and you'll find README.md file.

 cat README.md

/# Bandit Notes
Some notes for level29 of bandit.

/## credentials

- username: bandit29
- password: xxxxxxxxxx
 
To retrieve previous commits:

git log --oneline ./README.md

e2e1de5 (HEAD -> master, origin/master, origin/HEAD) fix info leak
2678cfa add missing data
9530d52 initial commit of README.md

These are all commits that the owners of this repo did. We can view the readme file at each:

git show 2678cfa:./README.md
/# Bandit Notes
Some notes for level29 of bandit.

/## credentials

- username: bandit29
- password: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0

And now you have the bandit29 password 😍🤯

## Voila!🎉
