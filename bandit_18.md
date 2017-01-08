#Bandit Level 18 → Level 19

##Level Goal

The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

##Commands you may need to solve this level

ssh, ls, cat

#Code Input
Open shell and login to server:
>$ ssh bandit18@bandit.labs.overthewire.org.

Type password from bandit17: kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

You'll automatically get logged out because once you run ssh it will read .bashrc which is modified to log you out. What you want to do is to login without having .bashrc being run. 
>$ ssh -t bandit18@bandit.labs.overthewire.org /bin/sh

Logging in with 'ssh -t' will create a remote "temporary" ssh connection. "/bin/sh" will run a bash shell (instead of the regular shell) which does not read .bashrc

Enter the password again and read the readme file:
>$ ls

>readme

>$ cat readme

>IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

Password to the next level: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
