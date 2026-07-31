# Level 19
Current user: bandit18

## Concept - SSH Login Without bashrc
We used to login into a bandit account using the typical ssh command. But in this level, they changed the .bashrc to log us out whenever we login via SSH.

This file is hidden and requires special prompts so we won't deal with changing it. We can, however, bypass its conditions with ssh by adding a condition in the ssh command.

## Commands - Only Two

ssh -t user@hostname /bin/sh : this command allows us to log in via the secure shell (SSH) without triggering a bashrc command

cat : to read the password


## Hint
Just use the ssh command above with the correct port and user.

## Solution
Command to execute:

ssh -t -p 2220 bandit18@bandit.labs.overthewire.org /bin/sh

Then enter bandit18 password from the previous level: OQxXZjELndr90zuhOTDYBEomI0SZITXI

You are in. Execute:

cat readme

And you have the password for bandit19!

KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI

## Voila!🎉
