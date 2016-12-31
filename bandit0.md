#Bandit Level 0

##Level Goal

The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.

##Commands you may need to solve this level

ssh

##Helpful Reading Material

Secure Shell (SSH) on Wikipedia
How to use SSH on wikiHow

#Bandit Level 0 → Level 1

##Level Goal

The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH to log into that level and continue the game.

##Commands you may need to solve this level

ls, cd, cat, file, du, find

##Code Input
//open shell 
>$ ssh bandit0@bandit.labs.overthewire.org. 
 
enter password: bandit0 
>$ ls
  
  >readme
  
the 'ls' command lists the file(s) in directory, in this case the file name is "readme"

>$ cat readme 

gives you the password to next level: boJ9jbbUNNfktd78OOpsqOltutMc3MY1
