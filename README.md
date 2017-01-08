#Bandit Level 17 → Level 18

##Level Goal

There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19

##Commands you may need to solve this level

cat, grep, ls, diff

#Code Input
>$ ls

> passwords.new passwords.old 

Use the diff command to compare the two textfiles:
>$ diff passwords.new passwords.old

>42c42

>kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

>---

>BS8bqB1kqkinKJjuxL6k072Qq9NRwQpR

"42c42" means line 42 in file1 needs to be changed to be the same as line 42 in file 2. "c" means change. Since our password is located in passwords.new, our password to the next level is:

kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
