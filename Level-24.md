# Level 24
Current user: bandit23

## Concept - Cron & Permissions 🤫
As introduced in the previous level, cron is a daemon process that executes scripts at a time interval. The catch is that cron is also specific to each user in a way that each user runs scripts at the specified time. So bandit23 has a crontab and bandit24 has a crontab.

In this level, we're given that bandit24 has a cron and we should take advantage of it. Meaning, we should run a script by the cron of bandit24 that'll lead us to the password of bandit24. But how do you get permission of reading bandit24's password if you're bandit23? This is what the cron of bandit24 helps us with. 😉


## Commands - The Typical...Not Much Though
Login into bandit23: ssh -p 2220 bandit23@bandit.labs.overthewire.org

Password of bandit23 : gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw

cd, cat, mkdir, ls -la, chmod, cp

## Hint
If the cron of bandit24 executes its scripts as bandit24, where should the script be? Read the scripts being executed by the cron of bandit24 and see what folder is being used. 

## Solution
Command to execute:

ls /etc/cron.d

cat  /etc/cron.d/cronjob_bandit24

Now read the script:

cat /usr/bin/cronjob_bandit24.sh

It seems gibberish but hold on 😫. This script checks /var/spool/bandit24/foo and executes the scripts in it as bandit24 but owned by bandit23...so we can do a script to get bandit24 password!

Let's begin:

Since the scripts are deleted once they are executed, then we're going to put them in a directory outside of bandit24 reach so we always have them.

cd /tmp

mkdir plotr

chmod 777 plotr   (this grants read write execute permissions for everyone)

cd ./plotr

nano myscript.sh

Here, an editor will open, write this in it:

#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/plotr/password24

Press ctrl+o, then enter, then ctrl + x to exit

Now copy (not move cause then what was the point) to the bandit24 cron directory of scripts:

cp myscript.sh /val/spool/bandit24/foo

Now wait a minute (run date to see current time)

Then, do cat password24

You should get bandit24 password:

hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv


## Voila!🎉
