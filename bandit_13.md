#Bandit Level 13 → Level 14

##Level Goal

The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

##Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##Helpful Reading Material

SSH/OpenSSH/Keys

#Code Input
Open shell and login to server:
>$ ssh bandit13@bandit.labs.overthewire.org.

Type password from bandit12: 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

>$ ls

> sshkey.private

For this level, we want to use ssh to connect as a localhost to the bandit14 server without a password. 
>$ ssh bandit14@localhost -i ~/sshkey.private

>Are you sure you want to continue connecting (yes/no)? yes

>$ cat /etc/bandit_pass/bandit14

>4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

password to next level: 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e

*note: We connect as a local host because we are already logged into the server through bandit13. Typing '-i' allows us to connect to the server without a password*
