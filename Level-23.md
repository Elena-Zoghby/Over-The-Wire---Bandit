# Level 23
Current user: bandit22

## Concept - Cron & Script Files
Cron is a time-based job scheduler that checks what tasks need to be executed and at what time. It runs in the background, sometimes referred to as cron daemon. In Linux, we have different folders containing the cron files, like crond, crondaily, and cronhourly.
In this level, we are asked to look into crond.

Script files are files containing text that the system executes as commands sequentially. In our case, we're looking for a script file that will help us in getting the required password.


## Commands - A Bunch of Them
Login into bandit22: ssh -p 2220 bandit22@bandit.labs.overthewire.org

Password of bandit22 : RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz

cd, cat, and the commands in the script file

## Hint
Go the directory mentioned in the level by using cd. View its contents using ls and decide which file is the most important one for this level. Then read the contents of the chosen file you will find a script file. Proceed by reading its contents 😉.

## Solution
Command to execute:

cd /etc/cron.d/

ls

Here you'll see multiple files including cronjob_bandit23

 cat cronjob_bandit22

You'll get:

@reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

``* * * * *`` bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

Then execute:

cat /usr/bin/cronjob_bandit23.sh

Output:

#!/bin/bash

myname=$(whoami)

mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget

These are commands executed to move the password from its original location to a temp file in the tmp directory. How can we know what is the file's name?

$ means command

myname=bandit23, since we're looking for bandit23 password not bandit22 😋

Execute:

echo I am user bandit23 | md5sum | cut -d ' ' -f 1

You'll get a string of characters:

8ca319486bfbbc3663ea0fbe81326349

This is the file's name (not the password, bare with me). To get the password, execute:

cat /tmp/8ca319486bfbbc3663ea0fbe81326349

Output (bandit23 PASSWORD):

gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw


## Voila!🎉
