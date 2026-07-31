# Level 14
Current user: bandit13

## Concept - SSH KEYS & AUTHENTICATION
Imagine this scenario: someone figured your password and is now logging into your accounts from where ever they like. Could you have prevented this? Yes, using what we call SSH keys. An SSH key is a mathematical number that you have, called private key, and the server have another one of it, called public key. You verify that it is you that's logging using your private key. So the server reads your private key and verifies your identity using your public key that they store. 

In this level, we are required to log into bandit14 without knowing the password and only using the SSH private key that we have a copy of. To access the password file on bandit14, we should be bandit14. Another way of verifying we are bandit14 without bandit14's pass is by having their private SSH key 🤯. Crazy right? That's why they made us have its private key (something no one does lol) so we log in as bandit14 and take the pass.

## Commands - Not A Lot This Time
cat: read a file's contents

scp: copy file from one machine to another over an encrypted channel

chmod 700: changing permissions so only me(user in charge of file) have full permissions to it (so no one else can read it)

ssh -i: login from localhost to another machine as a user using ssh private key

## Hint
Don't try to do as I do and login the server (bandit.labs.overthewire.org) while you are in the server (bandit13). First, make a copy of the SSH key on your local machine (localhost not bandit). Then, use it to login from the localhost. In other words, make a copy, exit, and try to login using the commands above.

## Solution
Command to execute:

scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .

chmod 700 sshkey.private

ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

Now you have successfully entered bandit14! To keep the password with you incase you needed to login again, do:

cat /etc/bandit_pass/bandit14

Password is:

aaWecNkG4FhxJQxz07uiwzVP6bJiYS65


## Voila!🎉
