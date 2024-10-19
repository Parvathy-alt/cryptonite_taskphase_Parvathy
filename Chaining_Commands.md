# CHAINING COMMANDS

## CHAINING WITH SEMICOLON 

We chain `/challenge/pwn` and `/challenge/college` using `;` the required command to get the flag is : `challenge/pwn; /challenge/college`
Flag : `pwn.college{8RZC24OT5hjRdN_fG--z6JAJqdI.dVTN4QDLwgTN0czW}`

## YOUR FIRST SHELL SCRIPT

First we create `x.sh` using `nano` command like so , `nano x.sh` then run the command : `/challenge/pwn` and `/challenge/college` and then run `bash x.sh` to get the flag 
Flag : `pwn.college{waVKfWADgPRGfCnqdHH4w73bimN.dFzN4QDLwgTN0czW}`

## REDIRECTING SCRIPT OUTPUT

Th output of `x.sh` is piped into ` /challenge/solve` which can be done by the command , `bash x.sh | /challenge/solve` 
Flag : `pwn.college{IhoPPJy1TA9uL1gGl5KB12Q3iOi.dhTM5QDLwgTN0czW}`

## EXECUTABLE SHELL SCRIPTS

We create a script called `script.sh` using `nano`in which we enter the command `/challenge/solve` after saving we enter `chmod +x script.sh` and run it using ` ./script.sh` 
Flag : `pwn.college{4oAMh8eBbdzIBbhn6MTN-NL08pZ.dRzNyUDLwgTN0czW}`



