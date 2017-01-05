#Bandit Level 8 → Level 9

##Level Goal

The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

##Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

##Helpful Reading Material

The unix commandline: pipes and redirects

#Code Input
Open shell and login to server:
>$ ssh bandit8@bandit.labs.overthewire.org.

Type password from bandit7: cvX2JJa4CFALtqS87jk27qwqGhBM9plV

>$ ls

> data.txt

Since we want to find a unique line in the text, type: 
>$ sort data.txt | uniq -uc

>1 UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

password to next level: UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR

*note: '-uc' will find the unique line and provide the count of the number of lines*
