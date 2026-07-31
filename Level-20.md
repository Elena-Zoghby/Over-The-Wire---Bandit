# Level 20
Current user: bandit19

## Concept - SetUID
How are we able to run sudo command so smoothly? It is the setuid bit that's changing under the hood. Setuid lets you change the permissions of a file by running it as its owner. It is a bit (s), that if were present in a  file permission, then you're allowed to change the file like the owner of it. Here, we need to view the password for bandit20 as the owner which is bandit20. To do this, we need to run the setuid binary file given to us in the home directory.


## Commands - Only One

./bandit20-do cat /etc/bandit_pass/bandit20

The setuid binary executables are run via: ./filename

Run ./bandit20-do alone and you'll find that you can run a command as another user. This user, in our case, is bandit20. So to run it all together, we do the complete command above.

## Hint
Just use the command above.

## Solution
Command to execute:

./bandit20-do cat /etc/bandit_pass/bandit20

And you have the password for bandit20!

4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA

## Voila!🎉
