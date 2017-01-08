#Bandit Level 16 → Level 17

##Level Goal

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

##Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##Helpful Reading Material

Port scanner on Wikipedia

#Code Input
Open shell and login to server:
>$ ssh bandit16@bandit.labs.overthewire.org.

Type password from bandit15: cluFn7wTiGryunymYOu4RcffSxQluehd

First, let's figure out which of the ports are 'open' and being listened to:
>$ nmap -p 31000-32000 localhost

>Starting Nmap 6.40 ( http://nmap.org ) at 2017-01-06 08:12 UTC

>Nmap scan report for localhost (127.0.0.1)

>Host is up (0.00038s latency).

>Not shown: 996 closed ports

>PORT      STATE SERVICE

>31046/tcp open  unknown

>31518/tcp open  unknown

>31691/tcp open  unknown

>31790/tcp open  unknown

>31960/tcp open  unknown

>Nmap done: 1 IP address (1 host up) scanned in 0.06 seconds

Next, we want to test each port to see whether or not is it speaks SSL:
>$ echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -connect localhost:31046 -ign_eof

error
>$ echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -connect localhost:31518 -ign_eof

speaks SSL but is not correct/infinite loop
>$ echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -connect localhost:31691 -ign_eof

error
>$ echo cluFn7wTiGryunymYOu4RcffSxQluehd | openssl s_client -connect localhost:31790 -ign_eof

>Correct!

We then recieve a RSA private key. Copy the password and then make a new temporary directory to save the password in: 
>$ mkdir /tmp/skey/

>$ cd /tmp/skey/

>$ touch sshkey.private

>$ vim sshkey.private

Paste the RSA password into vim and then exit with esc + : + x!

Next, we'll try connecting to the bandit17 server with our password text file:
>$ ssh -i sshkey.private bandit17@localhost

However, we'll get an error which says that our password is unprotected! We want to solve this by typing:
>$ chmod 600 sshkey.private

>$ ssh -i sshkey.private bandit17@localhost

And we are now connected to bandit17!

*note: touch will create a new file. 'chmod 600 sshkey.private' modifies the permissions so that only the owner can read and write the file*
