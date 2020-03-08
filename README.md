

#### To extract only a desired column from a file 
```
$ cut -c2 /etc/passwd
o
a
i
y
y
```
#### Range of characters can also be extracted from a file by specifying start and end position delimited with -. The following example extracts first 3 characters of each line from a file
```
$ cut -c1-5 /etc/passwd
root:
daemo
bin:x
sys:x
```
#### Instead of selecting x number of characters, if you like to extract a whole field, you can combine option -f and -d. The option -f specifies which field you want to extract, and the option -d specifies what is the field delimiter that is used in the input file.

```
$ cut -d ':' -f1 /etc/passwd
root
daemon
bin
sys
sync
games
man
```

#### You can also extract more than one fields from a file or stdout. Below example displays username and home directory of users who has the login shell as “/bin/bash”.

```
$ grep /bin/bash /etc/passwd | cut -d ':' -f 1,6
root:/root
tuttu:/home/tuttu
```
