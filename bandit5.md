#Bandit Level 5 → Level 6

##Level Goal

The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties: - human-readable - 1033 bytes in size - not executable

##Commands you may need to solve this level

ls, cd, cat, file, du, find

#Code Input
Open shell and login to server:
>$ ssh bandit5@bandit.labs.overthewire.org.

Type password from bandit1: koReBOKuIDDepwhWk7jZC0RTdopnAYKh

>$ls 

>$ cd inhere 

>$ls -l 

Twenty subdirectories will come up:
>total 80

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere00

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere01

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere02

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere03

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere04

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere05

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere06

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere07

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere08

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere09

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere10

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere11

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere12

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere13

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere14

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere15

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere16

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere17

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere18

>drwxr-x--- 2 root bandit5 4096 Nov 14  2014 maybehere19

We know that we want to file a file that is human readable, 1033 bytes, and is non-executable:
>$ find -size 1033c

> ./maybehere07/.file2

Let's see what file2 in subdirectory maybehere07 will print out
>$ cat ./maybehere07/.file2

password to next level: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

*note: '-l' prints the files in long list format and the 'c' in 1033c represents the file in bytes*
