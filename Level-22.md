# Level 22
Current user: bandit21

## Concept - Cron
Cron is a time-based job scheduler that checks what tasks need to be executed and at what time. It runs in the background, sometimes referred to as cron daemon. In Linux, we have different folders containing the cron files, like crond, crondaily, and cronhourly.
In this level, we are asked to look into crond.


## Commands - Maybe Two?
Login into bandit21: ssh -p 2220 bandit21@bandit.labs.overthewire.org

Password of bandit21 : bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY

cd, cat

## Hint
Go the directory mentioned in the level by using cd. View its contents using ls and decide which file is the most important one for this level. 

## Solution
Command to execute:

cd /etc/cron.d/

ls

Here you'll see multiple files including cronjob_bandit22

 cat cronjob_bandit22

Then, you'll notice that we have output with five stars. These stars mean that Linux is executing this program at hourly, minutely, and daily intervals. 

You'll also see the file that's being run so view its contents using cat:

cat /usr/bin/cronjob_bandit22.sh

The contents of the file are moved into another file in temporary directory. View it using:

cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

And you'll get the password for bandit22:

RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz


## Voila!🎉
