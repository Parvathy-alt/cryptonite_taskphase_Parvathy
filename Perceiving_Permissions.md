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






