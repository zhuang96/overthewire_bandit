#Bandit Level 11 → Level 12

##Level Goal

The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

##Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##Helpful Reading Material

Rot13 on Wikipedia

#Code Input
Open shell and login to server:
>$ ssh bandit11@bandit.labs.overthewire.org.

Type password from bandit10: IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR

>$ ls

> data.txt

The command 'tr' will manipulate the text and 'a-zA-Z' 'n-za-mN-ZA-M' rotates the letters 13 times:
>$ cat data.txt | tr 'a-zA-Z' 'n-za-mN-ZA-M'

>The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

password to next level: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
