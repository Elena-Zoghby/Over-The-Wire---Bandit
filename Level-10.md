# Level 10
Current user: bandit9

## Concept - Human Readable with Preceded Characters
A file can have different data types even though it's type is text; it could contain binary, numbers, characters, hidden urls... We have to spot the human readable aka text in the file and extract the "=" character.

## Commands
strings, grep, |

Those are the commands I found helpful; the others weren't much needed to be honest. Solutions differ in a way that we will now see there is multiple solution to this level and you are free to use whatever command you find easy to output.

Lucky for us, the strings command works by default with human readable text only, making our work easier. Using strings to filter out the human readable text and grep to search for "=" we're going to determine the password needed to move to the next level.


## Hint
Try combining the above two commands by the pipe.

## Solution
Command to execute:

strings data.txt | grep "="

You will get the password which is:

B0s2khmbT9u0geKuOoVGW3JZKhndE3BG

Enter level ten by executing:

exit

ssh -p 2220 bandit10@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
