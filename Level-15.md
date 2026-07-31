# Level 15
Current user: bandit14

## Concept - PORTS
You're probably opening multiple tabs for different websites and texting with your friend right now. Maybe you're also sending an e-mail to your boss to call in sick so you can solve OTW-Bandit without guilt. Ever wondered how you can communicate with all of these services from your computer? This concept is what we call Port number. Whenever you want to communicate with an service on the internet, you're choosing a certain port number to communicate with, like 80 for mail. Opening a connection with any destination must be defined by a port number and an IP address. 

What is an IP Address?

It is either a 4 or 6 numbers (or hex) separated by a . and are generated whenever you connect to a network. For example, over your home network you get an IP address that marks your device and lets servers know how to reach your phone. Go to a different router and the IP address changes. In other words, it is what defines us over the internet.

So a connection over TCP, which is highly reliable for data transfer, requires both a port number and IP address.


## Commands 
cat: read a file's contents

ssh: securely connect to a remote machine (transfer files over a secure channel using ssh keys discussed earlier)

nmap localhost: allows you to see what ports your machine (localhost) is connected to 

nc localhost portnumber: forms a receive/send pipe between your machine (localhost) and the portnumber only if the connection was already there (check via nmap)

## Hint
Localhost means the bandit14 user not your computer user 😁
## Solution
Command to execute:

ssh -p 2220 bandit14@bandit.labs.overthewire.org 

Enter bandit14 password: aaWecNkG4FhxJQxz07uiwzVP6bJiYS65

Now you are the user bandit14. This is localhost.

nmap localhost

You will find that a TCP connection is made with port 30000. So all is set for receiving and sending.

cat /etc/bandit_pass/bandit14 | nc localhost 30000

This passes the output of first statement (bandit14 password) to port 30000 and also receives the output on terminal.

You will get the output which is:

Correct!
pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7

This is bandit15 password. Enjoy!

## Voila!🎉
