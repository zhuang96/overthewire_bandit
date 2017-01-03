#Bandit Level 7 → Level 8

##Level Goal

The password for the next level is stored in the file data.txt next to the word millionth

##Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd

#Code Input
Open shell and login to server:
>$ ssh bandit7@bandit.labs.overthewire.org.

Type password from bandit1: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

>$ ls

> data.txt

Since there are no subdirectories to enter, let's use grep to find the word next to 'millionth':
>$ grep 'millionth' data.txt

>millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV

password to next level: cvX2JJa4CFALtqS87jk27qwqGhBM9plV
