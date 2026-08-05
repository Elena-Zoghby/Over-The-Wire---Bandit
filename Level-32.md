# Level 32
Current user: bandit31

## Concept - Git Ignore 
What if we wanted to push an API key or a password into git? Is there a way to make them invisible? Yes, using what we call gitignore. It is simply a file with permissions/restrictions that help us protect data.


## Commands - Three
git clone, git add, git commit, git push

## Hint
View .gitignore file (it's probably hidden) and see what types of files it ignores. What should we add to bypass these restrictions in git?

## Solution
Make sure you have exited from bandit servers by running exit.

Execute:

 git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo

 Enter password which is same as bandit29: 82NkymblpGBYmIXG6ZQ8YldBYstHpfUf

 Then check directories on your machine using cd

 You should see repo. Run ls and you'll find README.md file.

 cat README.md

Here you will find instructions on what you should do to get the password.
 
Create a key.txt file (in ~/repo) by running nano key.txt

Write in it : 'May I come in?'

Save and Exit

Now we want to push it to master but we can't push files with .txt extensions as mentioned in gitignore. To bypass them, we do:

git add -f key.txt

git commit -m "added key"

git push origin master

If you face troubles directly after the commit command, it's probably because you're not logged in as user and email. Log in and continue (use git config)

Password for bandit32:

pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT


## Voila!🎉
