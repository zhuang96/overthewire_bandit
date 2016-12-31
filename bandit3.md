#Bandit Level 3 → Level 4

##Level Goal

The password for the next level is stored in a hidden file in the inhere directory.

##Commands you may need to solve this level

ls, cd, cat, file, du, find

#Code Input
open shell and login to server:
>$ ssh bandit3@bandit.labs.overthewire.org.

type password from bandit1: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

if you type in 'ls' and you will see file "inhere"; type 'cd' to go into the directory:
>$ cd inhere

We know that there is hidden file in this directory; in order to view it we must type:
>$ls -a

three things will come up:
>.  ..  .hidden

view password:
>$ cat .hidden

password to next level: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

**note: "." means child directory (which is the directory you are currently in); ".." is the parent directory**
