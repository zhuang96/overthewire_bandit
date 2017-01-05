#Bandit Level 4 → Level 5

##Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

##Commands you may need to solve this level

ls, cd, cat, file, du, find

#Code Input
Open shell and login to server:
>$ ssh bandit4@bandit.labs.overthewire.org.

Type password from bandit3: pIwrPrtPN36QITSp3EQaw936yaFoFgAB

If you type in 'ls' and you will see file "inhere"; type 'cd' to go into the directory:
>$ cd inhere

We know that there is hidden file in this directory; in order to view it we must type:
>$ls 

Ten things will come up:
>-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09

If you try to cat certain file, it will print some funny looking text. To know which file to use, type: 
>$ file ./*

You'll see -file07 says ASCII text instead of data:
>$ cat ./-file07

password to next level: koReBOKuIDDepwhWk7jZC0RTdopnAYKh
