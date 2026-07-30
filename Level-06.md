# Level 6
Current user: bandit5

## Concept - Multiple Conditions
We previously saw how to utilize the file command to determine a file type, even multiple files' types. In this level, we're going to make use of the find command. Find is used to find a file/files according to specific conditions like file type, file size, and more.

We need a human readable file, with size equal to 1033 bytes, and not executable. 

## Commands
find, ls -a, cat, and cd

In this level, we have the inhere directory which contains 17 more directories  👀. To not traverse all the 17 directories and their multiple files, read the find documentation below to learn how to search in the system, not only in a directory:

https://askubuntu.com/questions/1108882/find-a-file-based-on-specifications

## Hint
Use . to search from the current directory and after it (in all its directories and files).

## Solution
First, write the conditions specified: 

-type f: human readable

-size 1033c: 1033 bytes in size

! -executable: not executable

Combine in one statement: -type f -size 1033c ! -executable

To not traverse all directories and files by hand, we use . as such:

find . -type f -size 1033c ! -executable

You will find that the file we're looking for is in ./inhere/maybehere07/.file2

Notice that it's hidden because it starts with a dot. So when using the cat instruction, we need to place "" around the file name to prevent the system from understanding it as directory.

Continue by : cat ./inhere/maybehere07/".file2"

You will get the password which is:

pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

Enter level six by executing:

exit

ssh -p 2220 bandit6@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
