# Level 9
Current user: bandit8

## Concept - Word Search With Duplicates
Searching for a word or specific sequence is easy, but doing it while having duplicates becomes harder. In this level, our job is to search for the only line that is not repeated. Similar to what we did in the previous level, here we also have to search the file but this time we don't have a specific word appending the password, only count.

## Commands
sort, uniq -u

Those are the commands I found helpful; the others weren't much needed to be honest. Solutions differ in a way that we will now see there is multiple solution to this level and you are free to use whatever command you find easy to output.

sort: sorts the text file according to the sequence specified by the user

uniq -u: usually used with another command's output to output only the non-duplicate text (which is what we need in this level).

| : pipe, used to combine output of one command and redirect it to the input of another. Very useful

## Hint
Try combining the above two commands by the pipe.

## Solution
Since we already know that there is only one unique non-duplicate text in the file, we're simply going to execute the command:

sort data.txt | uniq -u

You will get the password which is:

EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

Enter level nine by executing:

exit

ssh -p 2220 bandit9@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
