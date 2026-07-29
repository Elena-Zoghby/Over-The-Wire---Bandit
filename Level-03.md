# Level 3
Current user: bandit2

## Concept - Spaces in File Name
Spaces in filenames break command-line operations because shells use whitespace to separate arguments. When a program encounters an unquoted space, it interprets each word as a different file or instruction instead of a single path.

Remember in level 1-->2, we used -- to bypass dashes in a file's name. Similarly, we're going to use a specific character to bypass Spaces.

## Commands
The usual: ls and cat

The commands below are not necessary but might be helpful if you're lost:

Use pwd to know where you are

cd to move to another directory (cd /home/bandit2)

## Hint
To bypass the dash, we should use --

To bypass the spaces, we use another character. Learn about it here: 

https://www.google.com/search?q=spaces+in+filename

## Solution
First, list the files using ls. You should see a file named --spaces in this filename--.

Then, read its content and avoid the terminal mistaking it into option using -- in the cat command:

 cat -- /home/bandit2/"--spaces in this filename"

You can also use '' or \ to escape spaces but I found this the easiest way to read such file.

Here, you should be able to view the password to move to level 3:

7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

Enter level three by executing:

exit

ssh -p 2220 bandit3@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
