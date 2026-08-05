# Level 26
Current user: bandit25

## Concept - More Command & Shells
Every user in linux has the choice of choosing what shell to run their commands. In our case, bandit26 chose a different shell than the one we usually use which is bash. Not only that, but every time we try to log into bandit26 we get a welcome bandit26 banner than immediately logged out. We should find a way to disable being immediately logged out.


## Commands - Stay With Me 🙌
Login into bandit25: ssh -p 2220 bandit25@bandit.labs.overthewire.org

Password of bandit24 : SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P

ls, ssh, v (to open vim editor), cat /etc/shells to view shells of users, grep "^username:" /etc/passwd

## Hint
First to log into bandit26 we should have a pass/sshkey. Run ls and you will see that we have a ssh key for bandit26 so try logging in to discover what happens. Then, run grep "^bandit26:" /etc/passwd to figure out what shell bandit26 is using. Also, search what does the more command do and how to break it.

## Solution
Command to execute:

Copy sshkey into a local file on your pc (not bandit server).

Try logging in using sshkey:

ssh -i ~/.ssh/yourkeyfilename bandit26@bandit.labs.overthewire.org

And you're immediately logged out. Why? Because what is happening is that every time you log in bandit26, a text file is being displayed and once it finishes printing everything in your terminal it exits. This is how the more command works. More displays as much character as the terminal size is. 

So to break this loop, simply (i mean really simply), make your terminal smaller (just drag it into less size). This way you will see that the more is barely printing (you will see percentage next to it). Just like that, we prevented whole file from running by pausing it. 

Now while waiting, press v. This open the Vim editor. Then type: :set shell=/bin/bash

Then: :shell 

And now we have a shell to write commands as bandit26!

Password for bandit26:

jHdv2ELQhT22BkprMNDjybZDAkw1zeBJ

Stay here don't exit. We need this terminal for the next level!


## Voila!🎉
