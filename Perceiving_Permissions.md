# PERCEIVING PERMISSIONS

## CHANGING FILE OWNERSHIP 

In this challenge we change the owner the flag by running the command to "hacker" by running the command `chown hacker /flag ` then we run the command ` cat /flag` to get the flag 
Flag : `pwn.college{o3UTQ94FHyi_Z99isXoaqqOXX6s.dFTM2QDLwgTN0czW}`

## GROUPS AND FILES 

We us `chgrp hacker /flag` where `/flag` is the file location of the flga and "hacker" is user , after running this command we run `cat /flag` to get the flag. 
Flag : `pwn.college{4BgPoFEoNdl6cyptP7vTlR-PEIy.dFzNyUDLwgTN0czW}`

## FUN WITH GROUP NAMES 

The name of the group has been changed from "hacker" to a randomized one , which we can figure out by using the command `id` after which we will figure out the group is "grp366"
Commands we have to run to get the flag are as follows : 
`chgrp grp366 /flag`
`cat /flag`
Flag : `pwn.college{40KQdfBNB36c0GYzRktXXMWh14E.dJzNyUDLwgTN0czW}`

## CHANGING PERMISSIONS

We run the command `chmod o+r /flag` , we use `o+r` such that all the users can read the file ,`chmod` to change the mods after which `cat /flag`
Flag : `pwn.college{U9nH262Vp5LGDdP3N76mgSVPX0D.dNzNyUDLwgTN0czW}`

## EXECUTABLE FILES 

We first run  the command `chmod u+x /challenge/run` ; `u+x` becuase `/challenge/run` is not executable to the owner `hacker` , after which we run `/challenge/run` to get the flag 
Flag : `pwn.college{QBnN1QsjlJWbvjmESZ6QBh79cQ9.dJTM2QDLwgTN0czW}`

## PERMISSIONS TWEAKING PRACTICE

We first run : `/challenge/run`
Then we run the following set of commands : 

`chmod g-r /challenge/pwn`

`chmod u-r,o-r /challenge/pwn`

`chmod u+r,o+r /challenge/pwn`

`chmod g+rx /challenge/pwn`

` chmod u-rw,o-r /challenge/pwn`

`chmod o+rw /challenge/pwn`

`chmod o+x  /challenge/pwn`

`chmod u+w,g+w /challenge/pwn`

`chmod u+r /flag`

Then we run `cat /flag` to get the flag 
Flag : `pwn.college{0MjjB2KdpUk-iGkZ0m4FWfB7w3x.dBTM2QDLwgTN0czW}`

## PERMISSION SETTING PRACTISE

We first run : `/challenge/run`
Then we run the following set of commands : 

`chmod u=-,g+wx,o+wx /challenge/pwn`

`chmod u=x,g=x,o=x /challenge/pwn`

`chmod u=rw,g=-,o=- /challenge/pwn `

`chmod g=r,o-x /challenge/pwn `

`chmod u=w,g+rx,o+r /challenge/pwn `

`chmod u+r,g=w,o+w /challenge/pwn `

`chmod u+wx,o+w /challenge/pwn `

After we run `chmod u+r /flag` to make it accessible and `cat /flag` to get the flag 
Flag : `pwn.college{kNzCBIT5-RUtn3Kzi-dvBabjACJ.dJjN1QDLwgTN0czW}`

## THE SUID BIT

We set the SUID bit by running the command `chmod u+s /challenge/getroot` after which we run `/challenge/getroot` after which we'll get the output :
`SUCCESS! You have set the suid bit on this program, and it is running as root! `

`Here is your shell...`

`root@permissions~the-suid-bit:~#`

Then we run : `cat /flag` to get the flag : `pwn.college{A9BnUBR9FRDN3hCwqMBj6s034KN.dNTM2QDLwgTN0czW}`








