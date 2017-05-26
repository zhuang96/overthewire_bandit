#Bandit Level 19 → Level 20

##Level Goal

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

#Code Input
Open shell and login to server (you need to connect to port 2220 instead of 22):
>$ ssh bandit18@bandit.labs.overthewire.org -p 2220 

Type password from bandit18: 

You'll automatically get logged out because once you run ssh it will read .bashrc which is modified to log you out. What you want to do is to login without having .bashrc being run. 
>$ ssh -t bandit18@bandit.labs.overthewire.org /bin/sh

Logging in with 'ssh -t' will create a remote "temporary" ssh connection. "/bin/sh" will run a bash shell (instead of the regular shell) which does not read .bashrc

Enter the password again and read the readme file:
>$ ls

>readme

>$ cat readme

>IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x

Password to the next level: IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x
