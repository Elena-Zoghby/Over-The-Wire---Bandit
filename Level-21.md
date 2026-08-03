# Level 21
Current user: bandit20

## Concept - Client & Server
You're probably staring at your screen right now not understanding what is TMUX. Same. To put it in simple words, TMUX allows you to separate your terminal into sessions. This makes it possible to run two different sessions which is helpful in our case because we need a side to send the password and another one to receive and send back the next level's. Such a communication is a classic client-server communication where the Server listens and the Client requests. 


## Commands - Maybe Two?
Login into bandit20: ssh -p 2220 bandit20@bandit.labs.overthewire.org

Password of bandit20 : 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA

tmux : creates new session, click Ctrl + b then % to split terminal vertically to have two sessions 😉

nc : binds to a port (creates connection)

./suconnect <portnumber> : runs the SetUID binary file and connects to port waiting for correct password to be transmitted


## Hint
Play around with tmux. Don't rely on my definition/shortcuts for this command cause it's confusing at first. After understanding it, ask yourself which terminal is the server and which is the client?

## Solution
Command to execute:

tmux

Ctrl + b, %

Connect both terminals to bandit20 using SSH

In one terminal run: nc -l 8080

In the other terminal run: ./suconnect 8080

Send in the password for bandit20 in terminal 1 (the one with nc) 🙂

You should get in the second terminal:

Read: 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA 
Password matches, sending next password 

In the first terminal you'll receive the bandit21 password:

bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY

## Voila!🎉
