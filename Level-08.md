# Level 7
Current user: bandit7

## Concept - Word Search
We have that the password is next to the "millionth" word, but we don't know where that word is. The idea behind this level is to be able to find the desired word while scanning for any duplicates of it as to make sure there is only one unique password for the next level.

## Commands
grep, uniq -c, strings

Those are the commands I found helpful; the others weren't much needed to be honest. Solutions differ in a way that we will now see there is multiple solution to this level and you are free to use whatever command you find easy to output.

grep: searches a file for a specific occurrence and outputs the relative lines. Use it like this:

grep "word" filename

uniq -c: usually used with another command's output to output how many times a word is repeated. For example, we want to see how many times the word millionth was repeated:

grep "millionth" data.txt | uniq -c

If you're not familiar with the symbol |, it is called pipe. It sends the output of a command to another (grep's to uniq).

strings: it looks in a file to find any hardcoded characters or addresses to make them readable. They didn't mention any binary content in our file but it's worth looking into.

strings data.txt | grep "millionth"

## Hint
Use one of the commands above and you should directly get the password next to millionth.

## Solution
I guess the solution must be pretty straight forward by now, especially since I mentioned how to use each command. 

You can execute any of the commands above and you will get the output since millionth occurred only once in this file.

You will get the password which is:

VR1ljMayciFxbnUokuQmJFw6QC9VKtub

Enter level eight by executing:

exit

ssh -p 2220 bandit8@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
