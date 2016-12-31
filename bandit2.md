#Bandit Level 2 → Level 3

##Level Goal

The password for the next level is stored in a file called spaces in this filename located in the home directory

##Commands you may need to solve this level

ls, cd, cat, file, du, find

##Helpful Reading Material

Google Search for “spaces in filename”

#Code Input
open shell and login to server:
>$ ssh bandit2@bandit.labs.overthewire.org.

type password from bandit1: CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9

if you type in 'ls' and you will see file "spaces in this filename"

in order to view this filename with spaces, you must type:
>$ cat spaces\ in\ this\ filename

password to next level: UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK

**hint: if you hit tab, shell will fill in the rest of the file name for you ex:** *"sp" -tab- will become "spaces\ in\ this\ filename"*
