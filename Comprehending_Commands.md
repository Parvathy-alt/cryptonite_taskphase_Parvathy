# COMPREHENDING COMMANDS

## CAT COMMAND 

We learn about a very crucial command known as "cat" , it is used to concatenate  . To obtain the flag we use the cat command to concatenate the flag file in the home directory . 

## CATTING ABSOLUTE PATHS 

We use the cat command to concatenate the flag file from its absolute path like so : "cat /flag" to obtain the flag which marks the successful compeltion of the challenege 

## CATTING PRACTISE 

XXXXXXX

## GREPPING 

When the files we obtain out of concatenating become too complex we can use the grep command . 
The format for the greo command is as follows : "hacker@dojo:~$ grep SEARCH_STRING /path/to/file"
To obtain the flag the required line of command is as follows : "grep pwn.college /challenge/data.txt"

## LISTING FILES 

We learn about "ls" command which allows us to list the files present in our desktop , We were asked to list files present in a specific directory called "challenge" , on opening that files we will recieve the file location for the "/challenge/run" file 

## TOUCHING FILES 

To create blank files of our own we use the "touch" command .  In this level, we create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get the flag 

## REMOVING FILES 

As important it is to create a file , it is to delete it ,for that "rm" command is used . In this challenge , we create a file called
"delete_me" using touch command which we learned previosuly and then proceed to delete it using "rm" command . Later , run "/challenge/check"
to check whether the file has been successfully deleted or not . 

## HIDDEN FILES

## FILESYSTEM QUEST 

## MAKING DIRECTORIES 

We learn about a command called "mkdir" to make directories . In this challlenge we make a directory called "/tmp/pwn" in which we make a file called "college" and later run the code "/challenge/run" to check whether the file has been created succesfully and on completion we receive a flag 

## FINDING FILES

To find a file in the provided system we use "find" command . On running the command , "find / -name flag" , many files appear on the 
screen out of which we use "cat" commmand to find out which has the required flag 
In the given case the flag was found in the "/usr/lib/python3/dist-packages/magic/flag" file 
The flag was : pwn.college{wBFUcuFlmeYW2tQqIzDe0BJetqB.dJzM4QDLwgTN0czW}

## LINKING FILES 

In this challenge we are taught to link files to one another . Executing the follwing code will retrive us the flag which marks the successful completion of this challenge : 
ln -s /flag not-the-flag
/challenge/catflag








