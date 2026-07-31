# Level 18
Current user: bandit17

## Concept - Comparing Files
The idea here is to compare two files and find the changed line from the old passwords to the new one. The new line is the password.

## Commands 
diff [file1] [file2] : compares line by line the two files and outputs what needs to be changed from file1 to become like file2. So pay attention to order new and old in correct order.

## Hint
New passwords come before old passwords. Or vice versa. Just pay attention.

## Solution
Command to execute:

diff passwords.old passwords.new

You'll get: 

42c42
< icUh23IUytZLIYhcCaXL18agiSIqymBc
---
> OQxXZjELndr90zuhOTDYBEomI0SZITXI

The password for level 18 is the next line which is : 

OQxXZjELndr90zuhOTDYBEomI0SZITXI

Enter level 18 by running:

ssh bandit18@bandit.labs.overthewire.org -p 2220

And the password. Enjoy!

## Voila!🎉
