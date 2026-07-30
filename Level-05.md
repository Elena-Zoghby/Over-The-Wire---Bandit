# Level 5
Current user: bandit4

## Concept - File Types
A file could have many types like ascii text (human-readable), data, .zip, etc...

In Linux, we can view a file type without having to view the file. Using what we call the "magic number", a file type could be verified. A magic number represents the first few bytes of a file that should by convention belong to the file type which is claimed. For example, if a file says it's png, we can verify that by running file -i image.png. If the output is the PNG magic numbers (89504E470D0A1A0A), then this file's type is indeed PNG.

For this level, we are asked to find the only human readable file. So we know that file type we are looking for is ASCII.

## Commands
cd, ls, file, cat

file: command used to identify file type (even traverse through multiple files and find the type of each) without reading it, using its magic number.

file filename : gives you type of the file named filename

## Hint
After moving into the inhere directory, execute ls. You will find 10 files, but do you think we have to read them all? Is there a way to traverse through all files in a directory and display the type of each?

## Solution
First, navigate to the inhere directory using 

cd /home/bandit4/inhere

View available files using ls command. You will see 10 files.

If you type file -- -file00, you will get output: data. Which means that it's not human readable. You can repeat this command for each file or you could execute the command below, which goes through all files in the current directory and identifies the type of each:

file ./-*  

This command is used because we already know that the files have names starting with -

If we had more files which didn't begin with -, we execute file ./* .*

It matches hidden files and all file names safely✔

You should get that the only human readable file is file07. Then, use cat to read its content as such:

cat -- -file07

Password: 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

Enter level five by executing:

exit

ssh -p 2220 bandit5@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
