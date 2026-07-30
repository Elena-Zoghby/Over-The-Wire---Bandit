# Level 12
Current user: bandit11

## Concept - Rot13
Rot13, rotation by 13, is a form of encryption that was used in the 1980s as a form of security. Each alphabet character (lowercase and uppercase) is replaced by the character that comes after it by 13 positions in the alphabet (A-->N, Z-->M). Of-course nowadays we don't use it as a form of security anymore cause it became easily breakable.

So our job in this level is to decrypt the text in data.txt back to original. Since rot13 makes characters move by 13 positions so that's half the way from a full turn (26 characters), it's inverse is itself. In other words, to obtain original text, perform another rot13 on the text.

## Commands
tr, cat, |

Those are the commands I found helpful; the others weren't much needed to be honest. Solutions differ in a way that we will now see there is multiple solution to this level and you are free to use whatever command you find easy to output.

tr: command used to translate, replace characters, etc...

We need it in this level to replace the corresponding character by the rotated character by 13 positions. View what each character corresponds to via: https://en.wikipedia.org/wiki/ROT13 

cat is needed to read the data.txt content and feed it into tr using |


## Hint
A is replaced by N, Z replaced by M...

## Solution
Command to execute:

cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

You will get the output which is:

The password is GROozWPO8QyN0mGrjUkID0WCYkZiQxrN

Enter level twelve by executing:

exit

ssh -p 2220 bandit12@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
