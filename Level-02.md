# Level 2
Current user: bandit1

## Concept - Dashed files
A dash in Unix system, and especially in Linux language, is understood as option or flag for commands. For example, ls -a, -l, etc...
That's why files that have dashes in their names are not preferable.

To move to level 2, the password is located in a file named -. How can we bypass the dash convention and make the terminal understand it as file name and not as option?

## Commands
The usual: ls and cat

The commands below are not necessary but might be helpful if you're lost:

Use pwd to know where you are

cd to move to another directory (cd /home/bandit1)

## Hint
To bypass the dash, we should use a specific character with the cat command. Use this link to discover it: 

https://www.google.com/search?q=dashed+filename

## Solution
First, list the files using ls. Did you see the file named - ?

Then, read its content and avoid the terminal mistaking it into option using -- in the cat command:

 cat -- /home/bandit1/-

Here, you should be able to view the password to move to level 2:

PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

Enter level two by executing:

ssh -p 2220 bandit2@bandit.labs.overthewire.org

Enter password.

## Voila!🎉

