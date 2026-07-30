# Level 7
Current user: bandit6

## Concept - Users and Groups
The idea behind this level is dealing with users and groups in Linux. The root contains groups and users. To search for a file owned by a specific user and/or group, you would have to search in the entire system (starting from the root). Root in Linux is referred to as /

## Commands
find, ls -a, cat, and cd

To search in the entire system for a file of 33 bytes in size and owned by user bandit7 and group bandit6, we should move to the root directory by doing cd /

## Hint
Execute cd /

Then, search use find with the -user and -group conditions to narrow your search.

## Solution
First, as we discussed, execute: cd /

Then, to narrow your search down to the files with the conditions specified, execute:

find . -user bandit7 -group bandit6 -size 33c

You will a really ugly and long output due to permissions being denied. Don't worry we don't need them now. To remove them from your output, not remove the permission :) , execute:

find . -user bandit7 -group bandit6 -size 33c 2>/dev/null

Look closely, you will find this path: /var/lib/dpkg/info/bandit7.password

Write cat /var/lib/dpkg/info/bandit7.password

You will get the password which is:

Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3

Enter level seven by executing:

exit

ssh -p 2220 bandit7@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
