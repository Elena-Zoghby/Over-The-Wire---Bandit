# Level 31
Current user: bandit30

## Concept - Git & Commits 🎯 
Once we change something in git, we commit to the change. Git stores the new changes and the old ones in a way that you view the changes you applied. 


## Commands - Three
git clone, git show, cat/ls

## Hint
View latest commits and the README.md file. Nothing useful. Dig deep into each directory given under the /.git directory in the repo. You will find the password somewhere there...

## Solution
Make sure you have exited from bandit servers by running exit.

Execute:

 git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo

 Enter password which is same as bandit29: jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX

 Then check directories on your machine using cd

 You should see repo. Run ls and you'll find README.md file.

 cat README.md

Yeah empty file...
 
ls -a

cd ./.git

cat packed-refs

Here you will notice something called secret. To view it, run:

git show secret

You'll get the password for 31:

82NkymblpGBYmIXG6ZQ8YldBYstHpfUf


## Voila!🎉
