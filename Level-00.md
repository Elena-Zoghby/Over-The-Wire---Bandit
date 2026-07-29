# Level 0: Entry
Username to login: bandit0
Password to login: bandit0

## Concept - SSH
SSH (secure shell) is a protocol used to secure the communication between two remote interfaces by providing encryption over the files transferred, requests/responses exchanges (client-server), and is used to execute a command on a remote machine.
In this level, we are making use of SSH Client. We are trying to access the server of bandit at port 2220, and we will be able to do that since we have password and username.

## Commands
ssh command is used. Click here to think it through:https://manpages.ubuntu.com/manpages/noble/man1/ssh.1.html

## Hint
Remember we have port number (2220) and the address we're connecting to :  bandit.labs.overthewire.org, and the username: bandit0.
These three fields should be present in your first command.

## Solution
Since we have the hostname and port number, you might think that they are enough to connect. But it's not, since we can't connect with any username to the server. We can only login using the username bandit0 (at this level), otherwise we won't be allowed perission (our user, for example your username on your pc in Ubuntu, isn't listed in the permission accepted list).
Execute the following command:

ssh -p 2220 bandit0@bandit.labs.overthewire.org

which has the format of: ssh -p port_number username@hostname_or_ip
Then, enter the password: bandit0.

## Voila!🎉


