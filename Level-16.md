# Level 16
Current user: bandit15

## Concept - SSL/TLS ENCRYPTION
Although SSL is the older version, and TLS is the standard protocol used nowadays, they both are responsible for securing millions of user data traveled between user's computer and the server. Whenever you request or send data from your browser to a website, the browser asks the website to verify itself using what we call Certificate. TLS encrypts your data so even if hackers viewed it they won't understand it not be able to use it, and it forces websites to prove their identities.

## Commands 
openssl s_client: opens an SSL (encrypted) connection between your machine with a port number (here it is 30001)

ssh: securely connect to a remote machine (transfer files over a secure channel using ssh keys discussed earlier)

## Hint
Open an encrypted connection with port 30001 and enter bandit15 password.

## Solution
Command to execute:

ssh -p 2220 bandit15@bandit.labs.overthewire.org 

Enter bandit14 password: pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7

Now you are the user bandit15. This is localhost. Now execute:

openssl s_client localhost:30001

You will get the output to enter bandit15 password. Enter it.

You will now get the output needed:

Correct!
kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

This is bandit16 password. Enjoy!

## Voila!🎉
