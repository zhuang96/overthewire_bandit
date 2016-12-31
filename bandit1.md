#Bandit Level 1 → Level 2

##Level Goal

The password for the next level is stored in a file called - located in the home directory

##Commands you may need to solve this level

ls, cd, cat, file, du, find

##Helpful Reading Material

Google Search for “dashed filename”
Advanced Bash-scripting Guide - Chapter 3 - Special Characters

#Code Input
>$ ssh bandit1@bandit.labs.overthewire.org.

type password from bandit0: boJ9jbbUNNfktd78OOpsqOltutMc3MY1

if you type in 'ls' and you will see file "-"

in order to view this dashed filename, you must type:
>$ cat ./-

password to next level: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
