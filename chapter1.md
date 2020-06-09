# chapter 1 the shell
### question 1 Create a new directory called missing under /tmp.
 
### answers:
 ```bash 
       $ cd / # go to root 
       $ cd tmp # go to tmp from root
       mkdir missing # creates a new directory under tmp
 ```

 
 ### question 2 Look up the touch program. The man program is your friend.
 
 ### answers:
 ``` bash
  $ man touch # allows to look program touch
```

### question 3 Use touch to create a new file called semester in missing.

### answers:
``` bash 
       $ cd / # go to root.  
       $ cd tmp # go to tmp.
       $ cd missing # go to missing.
       $ touch semester # create a file semester.
```

 ### question 4   Write the following into that file, one line at a time:    
 ### answer:
 ``` bash
       echo '#!/bin/sh' > question4.txt # > add output of echo to text file single quote '' as special character are used like #!
        echo "curl --head --silent https://missing.csail.mit.edu" >> question4.txt # >> appends to exesting file
        cat question4.txt #reads file
 ```       
### question 5 Try to execute the file, i.e. type the path to the script (./semester) into your shell and press enter. Understand why it doesn’t work by consulting the output of ls.
### answers: 
        permission denied as there is no permission for exucting that file. to check permission follow the steps below
 ``` bash
        $ cd / # go to root.  
        $ cd tmp # go to tmp.
        $ cd missing # go to missing.
        $ ls -l # detail list of files
```
### question 6
### answer :       
        to excute the file semseter 
 ``` bash       
        $ cd / # go to root.  
        $ cd tmp # go to tmp.
        $ cd missing # go to missing.
        $ sh semester # excutes the file no error as act as super user
 ```       
### question 7 look up chmod
###   answer  
``` bash
       $ man chmod # allows to look up chmod
```     
### question 8 Use chmod to make it possible to run the command ./semester rather than having to type sh semester. How does your shell know that the file is supposed to be interpreted using sh? See this page on the shebang line for more information.
### answer
``` bash
 $ chmod +x semester # change the bit to exuctabel mode whcih allows for everyone to excute
```
 ###  question 9 Use | and > to write the “last modified” date output by semester into a file called last-modified.txt in your home directory.
   
### answers:
``` bash
  $ ls -l semester | > lastmodified.txt # ls -1 allow to get the last modified date of the file and then output is typed in a file lastmodified.txt
```
#### the end
