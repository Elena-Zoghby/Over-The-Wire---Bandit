# Level 3
Current user: bandit3

## Concept - Hidden Files
Hidden files are files that are not shown directly using the typical commands. They benefit users for hiding keys or credentials. Anyway, to view hidden files, we execute the ls -a command where -a stands for all.

## Commands
ls -a, cat, and cd

In this level, the password is in a hidden file in a directory called inhere. Use cd to go to inhere directory:

cd /home/bandit3/inhere

## Hint
Once in inhere directory, execute ls -a command to view what files are hidden. This command outputs by default two outputs and the hidden files/directories. 

.: represents the current directory

..: represents the parent directory

The . means this file is hidden. So, what other than the defaults did you see? Can you use cat to read its content?

## Solution
First, navigate to the inhere directory using 

cd /home/bandit3/inhere

then, list the hidden files using ls -a. You should see . .. ...Hiding-From-You

The dot in the beginning of the file name indicates that this file is hidden. The presence of . in the beginning of the file name makes the dashes in it safe to read so the system won't understand them as flags.

Read its content using:

cat ...Hiding-From-You

You should see the password for level 4: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

Enter level four by executing:

exit

ssh -p 2220 bandit4@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
