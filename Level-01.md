# Level 1
Current user: bandit0

## Concept - Files
The concept here is simple. Find a file and read its contents. To do that, make sure you're already logged in bandit0. 

## Commands
ls: to find the available files & sub-directories located in the directory you are in. (you can even try ls-a to find hidden files, but you don't need it here)

cat: (short for concatenate) to read a file's contents and display them directly into the terminal. Usage: cat filepath

## Hint
The password is in a readme file in the home directory. First, check are you in the home directory of bandit0? Second, what are the available files & directories in this home directory? (remember what command to use...). Did you find the readme file? What command should be sued to display its contents?

## Solution
You should by default be in the home directory. If no, navigate there using:

cd /home/bandit0

After being there, list the files + directories using:
ls

You should get on your terminal readme. This is the file with the password. To read its content, execute:

cat /home/bandit0/readme

Then save the password on your local machine as to not lose it later. Type exit in the terminal of ubuntu to exit bandit0 and login as bandit1. Everytime you should exit the current level to login the new one. Login as bandit1 using:

ssh -p 2220 bandit1@bandit.labs.overthewire.org

Password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

## Voila!🎉


