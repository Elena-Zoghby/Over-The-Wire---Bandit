# Level 13
Current user: bandit12

## Concept - HEX DUMP, ZIP, & TAR
If you were ever dealing with multiple files in a folder and you felt the need to combine them neatly in one file 😃, in Linux, this is what we call TAR archive. Tar is simply a way to combine your files/folders into one sharable file. 

To save up space, on any OS, we compress the data. In Linux, to compress the data (in our case tar archive), we use either gzip or bzip2. Bzip2 is slower than gzip but better as compression. 

Hex dump represents the way a file is written which is in hexadecimals. The hex dump file representation doesn't signify anything to us in this level, it's just a way of representing the data. In other words, viewing in a hex dump format, won't give us an ASCII text that might lead us to the password.

How they all work together? 

You would combine multiple files in a tar archive. Then, compress them using either way of compression from those mentioned above. You have the choice to view in hex dump format or change to this format.

## Commands - A Lot of Them 🤷‍♀️
mktemp -d: used to create temporary directories in the current directory

cp: used to copy a file to another directory as to not lose the original file

file: view a file's content type (very useful to know what command to execute next)

ls: list files/directories in the current directory

xxd -r: used to revert a hex dump file into binary file, useful to know if compressed

mv: used to create a file from another file, mainly for changing extensions in files (bin to gz)

bzip2 -d : used to unzip a bzip2 file

gzip -d : used to unzip a gzip compressed file

tar -xf : used to extract contents of a tar archive

cat: used to display a file's content


## Hint
Our password is hidden in a file. This file was originally compressed with multiple formats (gzip, bzip2, tar). Start by creating temporary directory and a copy of the data.txt file in this directory. Check it's content. Convert to binary. View the type again. Is it compressed? How can we unzip ? Should we change the file's extension before? 

## Solution
Command to execute:

mktemp -d

cp data.txt /tmp/tmp.zZSQS8fWmX

cd /tmp/tmp.zZSQS8fWmX

ls

xxd -r data.txt > output.txt

file output.txt

mv output.txt output.gz

ls

file output

mv output.gz output.bz2

bzip2 -d output.bz2

ls

file output

mv output output.gz

gzip -d output.gz

ls

file output

tar -xf output

file data5.bin

tar -xf data5.bin

file data6.bin

mv data6.bin data6.bz2

bzip2 -d data6.bz2

file data6

tar -xf data6

file data8.bin

mv data8.bin data8.gz

gzip -d data8.gz

file data8

cat data8


You will get the output which is:

The password is qQYQiHOBPR8zR61qxYqX45quvihF2uzk

(finally)
Enter level thirteen by executing:

exit

ssh -p 2220 bandit13@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
