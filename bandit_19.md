#Bandit Level 19 → Level 20

##Level Goal

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

#Code Input
Open shell and login to server (you need to connect to port 2220 instead of 22):
>$ ssh bandit19@bandit.labs.overthewire.org -p 2220 

Type password from bandit18: 
>IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

After typing 'ls', we see that there is a locked directory (bandit20-do). Using the command line ls -l, we can figure out what type of owner of the file: 
>$ ls -l 

We get:
total 8
-rwsr-x--- 1 bandit20 bandit19 7370 Nov 14  2014 bandit20-do

To get the password, type in:
>$ ./bandit20-do cat /etc/bandit_pass/bandit20

Password to the next level: GbKksEFF4yrVs6il55v6gwY5aVje5f0j
