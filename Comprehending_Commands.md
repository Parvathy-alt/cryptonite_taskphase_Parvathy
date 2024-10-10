# COMPREHENDING COMMANDS

## CAT COMMAND 

We learn about a very crucial command known as "cat" , it is used to concatenate  . To obtain the flag we use the cat command to concatenate the flag file in the home directory . 
Flag : `pwn.college{Y6pw3DtCARn5wQoanxHFMGXbkK_.dFzN1QDLwgTN0czW}`

## CATTING ABSOLUTE PATHS 

We use the cat command to concatenate the flag file from its absolute path like so : cat /flag" to obtain the flag which marks the successful compeltion of the challenege 
Flag : `pwn.college{8Bx1vgHmuBQaN6KiQdalgR6dHti.dlTM5QDLwgTN0czW}`


## MORE CATTING PRACTISE 

We come to know the location fo the `flag` file is : `/usr/share/dpkg/flag` , then we use the following command to retrieve the flag : 
` cat /usr/share/dpkg/flag` 
Flag : `pwn.college{0nj_U2So9CSVqtB6tx2jogxJ5--.dBjM5QDLwgTN0czW}`

## GREPPING 

When the files we obtain out of concatenating become too complex we can use the grep command . 
The format for the greo command is as follows : `hacker@dojo:~$ grep SEARCH_STRING /path/to/file"`
To obtain the flag the required line of command is as follows : `grep pwn.college /challenge/data.txt"`
Flag : `pwn.college{Y-hCItgkclHTcCsnWpoC9Axjr_c.ddTM4QDLwgTN0czW}`

## LISTING FILES 

We learn about "ls" command which allows us to list the files present in our desktop , We were asked to list files present in a specific directory called "challenge" , on opening that files we will recieve the file location for the `/challenge/run` file . Which is 
`26860-renamed-run-27029`
Hence we do the following commands :
` cd /challenge`
` ls`
`./26860-renamed-run-27029`
Flag : `pwn.college{UaDTnPL-qLnlLu2aIR2GpCO6dZ7.dhjM4QDLwgTN0czW}`

## TOUCHING FILES 

To create blank files of our own we use the "touch" command .  In this level, we create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get the flag 
Flag: `pwn.college{I4drQUrzL6X0S0ElwUW95oULoU2.dBzM4QDLwgTN0czW}`

## REMOVING FILES 

As important it is to create a file , it is to delete it ,for that "rm" command is used . In this challenge , we create a file called
"delete_me" using touch command which we learned previosuly and then proceed to delete it using "rm" command . Later , run "/challenge/check"
to check whether the file has been successfully deleted or not . 
Flag : `pwn.college{cDjL-XQdAsw1JLjF8jh0Ci-VqaD.dZTOwUDLwgTN0czW}`

## HIDDEN FILES

We us the `ls -a` command to access the "hidden files" in the system , after running which we get a flag address ie `.flag-130802970017550`
Therefore the run the following lines of command to get the flag 
`cd /
ls -a
cat .flag-130802970017550`
Flag : `pwn.college{oHR6b2C4e3rIZX69lVnMPl-Q2Sh.dBTN4QDLwgTN0czW}`

## FILESYSTEM QUEST 

This was quite a quite lengthy execution process , but at last I managed to get the flag 
First we start with the root directory `cd /` then we use the `ls` command to list all the files present in the root directory 
Then we read the files and cat a file called `CLUE` , then ` cd  /usr/share/help/ko`

After which we `ls` again to find the file `BRIEF` 
`cat BRIEF` reads:
`Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/send2trash/__pycache__
The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
`
Then  `cd /usr/local/lib/python3.8/dist-packages/send2trash/__pycache__`  and `ls-a`
reads a set of files out of which we use ` cat .ALERT` to get the next output :
`Congratulations, you found the clue!
The next clue is in: /usr/lib/python3/dist-packages/sage/numerical/backends/__pycache__`

Then we run `cd  /usr/lib/python3/dist-packages/sage/numerical/backends/__pycache__` and ` ls -a`
according to which  we get `cat NUGGET` and the output 
`Great sleuthing!
The next clue is in: /usr/lib/jvm/java-17-openjdk-amd64/legal/java.rmi`
and just go ahead till we reach `cat EVIDENCE` which finally will give us the required flag 
which is : `pwn.college{UmcNQI9iibhVYdJRZBI6GqoV2GK.dljM4QDLwgTN0czW}`


## MAKING DIRECTORIES 

We learn about a command called "mkdir" to make directories . In this challlenge we make a directory called "/tmp/pwn" in which we make a file called "college" and later run the code "/challenge/run" to check whether the file has been created succesfully and on completion we receive a flag 
Flag : `pwn.college{cYcGI1mTV-BA3yNlSUsSL8IRzDo.dFzM4QDLwgTN0czW}`

## FINDING FILES

To find a file in the provided system we use "find" command . On running the command , "find / -name flag" , many files appear on the 
screen out of which we use "cat" commmand to find out which has the required flag 
In the given case the flag was found in the "/usr/lib/python3/dist-packages/magic/flag" file 
The flag was : pwn.college{wBFUcuFlmeYW2tQqIzDe0BJetqB.dJzM4QDLwgTN0czW}

## LINKING FILES 

In this challenge we are taught to link files to one another . Executing the follwing code will retrive us the flag which marks the successful completion of this challenge : 
`ln -s /flag not-the-flag`
`/challenge/catflag`
Flag : `pwn.college{kDfFXk0uRLO-3dbrgexuZ_IoiU9.dlTM1UDLwgTN0czW}`








