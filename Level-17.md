# Level 17
Current user: bandit16

## Concept - SSL/TLS ENCRYPTION + PRIVATE KEYS
As we have previously mentioned how our browser uses TLS encryption to safely communicate with websites, here it is our job to find what server can offer us this level on encryption (since we need to login using a private ssh key), and which can respond in the way we want it to. 

## Commands 
nmap -p 31000-32000 localhost : scans wat ports in range 31000 to 32000 is communicating with our machine, in this case the bandit16 user

openssl s_client: opens an SSL (encrypted) connection between your machine with a port number. If the port's server doesn't support TLS encryption you will not get a certificate verification.

ssh: securely connect to a remote machine (transfer files over a secure channel using ssh keys discussed earlier)

chmod 600: protects the private key on your machine and is required by servers who open connection with your host as to not risk security leaks.

cat: read a file's contents 

## Hint
Try opening an SSL/TLS connection with each of the ports that resulted from nmap command. Which ones aren't compatible? For the ones that are, can you directly paste bandit16 password? Or there is a condition you should include in the openssl command? Google it.

## Solution
Command to execute:

ssh -p 2220 bandit16@bandit.labs.overthewire.org 

Enter bandit14 password: kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

Now you are the user bandit16. This is localhost. Now execute:

nmap -p 31000-32000 localhost

Here, you will see that we have several connections connected with our localhost and these ports. 

Run: openssl s_client -connect localhost:portnumber -nocommands

For each port number that resulted from the NMAP.

Why add -connect and -nocommands? Because our password for bandit16 which is required to get the credentials for this level, starts with 'k'. This triggers a key rotation and therefore a key update at their end (the server's end). 

Enter the bandit16 password. You will get the private ssh key required to enter bandit17.

Copy it and paste it in a file on your local machine (since you can only login a server once you are out of it lol).

Run:

nano ~/.ssh/key17

Enter the certificate (with the end and opening) in it. Save and exit. 

Make sure only you can read the file and no one else using:

chmod 600 ~/.ssh/key17

Then, you're safe to transfer it. Run

 ssh -i ~/.ssh/key17 bandit17@bandit.labs.overthewire.org -p 2220

And you're in!

To have the password of bandit 17, run:

cat /etc/band_pass/bandit17

You'll get: 

pWXMAZoxGC8JmDMfmT5MGEsobMM3vnj2


This is bandit17 password. Enjoy!

## Voila!🎉
