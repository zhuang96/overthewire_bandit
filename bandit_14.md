#Bandit Level 14 → Level 15

##Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

##Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##Helpful Reading Material

##How the Internet works in 5 minutes (YouTube) (Not completely accurate, but good enough for beginners)
IP Addresses
IP Address on Wikipedia
Localhost on Wikipedia
Ports
Port (computer networking) on Wikipedia

#Code Input
Open shell and login to server:
>$ ssh bandit14@bandit.labs.overthewire.org.

Type password from bandit13: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

Let's use echo to "talk" to the server (we can either use 'localhost' or '127.0.0.1' which is the IP address):
>$ echo -n 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e | nc localhost 30000 

> Correct!

>BfMYroe26WYalil77FoDi9qh59eK5xNr

password to next level: BfMYroe26WYalil77FoDi9qh59eK5xNr
