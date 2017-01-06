#Bandit Level 12 → Level 13

##Level Goal

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

##Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv

##Helpful Reading Material

Hex dump on Wikipedia

#Code Input
Open shell and login to server:
>$ ssh bandit12@bandit.labs.overthewire.org.

Type password from bandit11: 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu

>$ ls

> data.txt

Not going to lie, but this level requires a lot more research than the other levels. Basically, data.txt is a hexdump that is compressed. We want to decompress this file in a temporary directory that we will create, and then repeated decompress different types of files. Make sure to know the appropriate file extensions that correspond to the required decompression of the file. 

First we want to make a temporary directory, move data.txt into it and then work from the newly created directory:
>$ mkdir /tmp/zhuang

>$ cp data.txt /tmp/zhuang

>$ cd /tmp/zhuang

Now we are in the new directory. We know that data.txt is hexdump, so we should use the xxd command to reverse it back into binary and rename it:
>$ xxd -r data.txt > bin

>$ ls

>bin data.txt

From here on out, we'll be doing a lot of idenifying file types (use file command), appending the appropriate file extension (use mv command along with gz, bz2), and decompressing (use gzip, bzip2, tar):

>$ file bin

>bin: gzip compressed data, was "data2.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression

>$ mv bin bin.gz

>$ gzip -d bin.gz 

>$file bin

>bin: bzip2 compressed data, block size = 900k

>$ mv bin bin.bz2

>$ bzip2 -d bin.bz2 

>$ file bin

>bin: gzip compressed data, was "data4.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression

>$ mv bin bin.gz

>$ gzip -d bin.gz 

>$ file bin

>bin: POSIX tar archive (GNU)

>$ tar -xvf bin

>data5.bin

>$ file data5.bin 

>data5.bin: POSIX tar archive (GNU)

>$ tar -xvf data5.bin

>data6.bin

>file data6.bin 

>data6: POSIX tar archive (GNU)

>$ tar -xvf data6

>data8.bin

>$ file data8.bin 

>data8.bin: gzip compressed data, was "data9.bin", from Unix, last modified: Fri Nov 14 10:32:20 2014, max compression

>$ mv data8.bin data8.gz

>$ gzip -d data8.gz 

>file data8

>data8: ASCII text

>$ cat data8

>The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL

Hooray! Although that was a bit of a struggle, we made it!
