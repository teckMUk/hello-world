### question 1:Read man ls and write an ls command that lists files in the following manner

1. Includes all files, including hidden files
2. Sizes are listed in human readable format (e.g. 454M instead of 454279954)
3. Files are ordered by recency
4. Output is colorized

### answer:
``` bash
   $ ls -Ahlc --color 
```
### question 2: Write bash functions marco and polo that do the following. Whenever you execute marco the current working directory should be saved in some manner, then when you execute polo, no matter what directory you are in, polo should cd you back to the directory where you executed marco. For ease of debugging you can write the code in a file marco.sh and (re)load the definitions to your shell by executing source marco.sh.

### answer:
#### marco.sh
``` bash
#!/bin/bash
marco () {
    cdir=&(pwd)
}
```
#### polo.sh
``` bash
#!/bin/bash
marco () {
    cd &cdir
}
```
``` bash
$ source marco.sh // this is the way of excuting the fuction
$ source polo.sh 
```
### question 3

### anwser:

### question 5

### answer:
``` bash 
$ find . -type d | xargs ls -lt
```
