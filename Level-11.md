# Level 11
Current user: bandit10

## Concept - Base64 Encoding
Base 64 encoding is a type of encoding that represents a 6-bit segment of bytes into one of the 64 characters. These characters range from uppercase and lowercase alphabet to digits (0 to 9), and +,/ . This type of encoding is primarily used to transfer binary data as text and to encode any important credentials for safe transmission over the internet.

In this level, we have the encoded version of the text and we want to decode it in order to get the password.

## Commands
cat (if you need to view the file's encoded text), base64

Those are the commands I found helpful; the others weren't much needed to be honest. Solutions differ in a way that we will now see there is multiple solution to this level and you are free to use whatever command you find easy to output.

To view the encoded text in the data.txt run: cat data.txt

base64 -d: lets you decode the encoded text, by working oppositely to how the encoding works. Contrary to what you might be thinking, it doesn't take one character, it takes 4 ASCII characters and breaks each into 6-bit representation which results into 24-bit stream. Then proceeds into splitting into 3 groups of 8-bit (byte) segments to match to their original text. 

---Skip this part if you're not interested in the math---

The encoded text in our case has 68 total characters. Each character is made up of 6-bits. Split each character into 6-bits and combine every 8 bits together to form the original character. Do the math you will find that we should get a 51 character output, while what we actually got is 48 characters. How? 

Turns out that our encoded text had two equal signs in its end as a form of padding (adding characters to make the text-size as requested). So remove these two characters and you will get 49.5 characters as decoded output. But in practice we can't have half a bit nor have total number of bits not divisible by 8. That's why you get a 48 output text which is the closest number divisible by 8. 


## Hint
It's really easier than you think. Run the command of base64 -d by reading how: 

https://www.google.com/search?q=base64+linux&sxsrf=APpeQntQJTl08OA0Sp6te-2O7XhbJ3y1hQ%3A1785391344092 

## Solution
Command to execute:

base64 -d data.txt

You will get the output:

The password is pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro

Enter level eleven by executing:

exit

ssh -p 2220 bandit11@bandit.labs.overthewire.org

Enter password above.

## Voila!🎉
