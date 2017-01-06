#Bandit Level 15 → Level 16

##Level Goal

The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption.

Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…

##Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap

##Helpful Reading Material

Secure Socket Layer/Transport Layer Security on Wikipedia
OpenSSL Cookbook - Testing with OpenSSL

#Code Input
Open shell and login to server:
>$ ssh bandit15@bandit.labs.overthewire.org.

Type password from bandit14: BfMYroe26WYalil77FoDi9qh59eK5xNr

After reading through the OpenSSL guide and using the hint from the description, this is the command I used: 
>$ echo BfMYroe26WYalil77FoDi9qh59eK5xNr | openssl s_client -connect localhost:30001 -ign_eof

You'll see information regarding the connection and this at the end: 
> Correct!

>cluFn7wTiGryunymYOu4RcffSxQluehd

>read:errno=0

password to next level: cluFn7wTiGryunymYOu4RcffSxQluehd

*note: I used echo to "talk" to the server, and this helped get rid of the 'Read R BLOCK' error. Using '-ign_eof' got rid of the HEARTBEAT error. HEARTBEAT seems to have a keep-alive function which verifies both ends of the connection.*
