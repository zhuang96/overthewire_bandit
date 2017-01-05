#Bandit Level 9 → Level 10

##Level Goal

The password for the next level is stored in the file data.txt in one of the few human-readable strings, beginning with several ‘=’ characters.

##Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

#Code Input
Open shell and login to server:
>$ ssh bandit9@bandit.labs.overthewire.org.

Type password from bandit8: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

>$ ls

> data.txt

To print the line that begins with several '=' characters, lets type in: 
>$ strings data.txt | grep '^==='

>========== password

>========== ism

>========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

password to next level: truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk

*note: strings will print out the line and '^' means the line starts with*
