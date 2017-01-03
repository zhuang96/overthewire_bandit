#Bandit Level 6 → Level 7

##Level Goal

The password for the next level is stored somewhere on the server and has all of the following properties: - owned by user bandit7 - owned by group bandit6 - 33 bytes in size

##Commands you may need to solve this level

ls, cd, cat, file, du, find, grep

#Code Input
Open shell and login to server:
>$ ssh bandit6@bandit.labs.overthewire.org.

Type password from bandit1: DXjZPULLxYr17uwoI01bNLQbtFemEgo7

Since there are no subdirectories to enter, let's find the file that is owned by user bandit7, group bandit6 and is 33 bytes in size
>find / -user bandit7 -group bandit6 -size 33c

You'll see a long list of files with "permission denied", but there will be one line that is not:
>/var/lib/dpkg/info/bandit7.password

Let's see what it will print out: 
>$ cat /var/lib/dpkg/info/bandit7.password

password to next level: HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

