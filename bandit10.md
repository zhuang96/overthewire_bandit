#Bandit Level 10 → Level 11

##Level Goal

The password for the next level is stored in the file data.txt, which contains base64 encoded data

##Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##Helpful Reading Material

Base64 on Wikipedia

#Code Input
Open shell and login to server:
>$ ssh bandit10@bandit.labs.overthewire.org.

Type password from bandit9: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

>$ ls

> data.txt

Base64 is an encoding scheme which represents binary data in ASCII string format. We want to decode the base64 encoded data:
>$ base64 -d data.txt 

>The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

password to next level: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

*note: -d will decode the text*
