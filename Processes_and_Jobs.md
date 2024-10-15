# PROCESSES AND JOBS 

## LISTING PROCESSES

We learned about ps command which stands for "process snapshot" or "process status" , it allows us to monitor the status of running processes on a system . We can use arguments to follow
along the ps command such as " ps -ef" and "ps aux"
To successfully complete the following challenge we run the command : 
`ps -ef`
And we are met with the output : 

```UID          PID    PPID  C STIME TTY          TIME CMD```

```root           1       0  0 00:32 ?        00:00:00 /sbin/docker-init -- /nix/va```

```root           7       1  0 00:32 ?        00:00:00 /run/dojo/bin/sleep 6h```

```root          68       1  0 00:32 ?        00:00:00 /challenge/27974-run-6586```

```root          72      68  0 00:32 ?        00:00:00 sleep 6h```

```hacker        73       0  0 00:32 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint```

```hacker        90      73  0 00:32 pts/0    00:00:00 ps -ef```

From which we run the command `/challenge/27974-run-6586` to get the flag which is : `pwn.college{8VzuePiJM-fTF4nfkLMzTItBVKP.dhzM4QDLwgTN0czW}`

## KILLING PROCESSES

We learn abou `kill` and `sleep` command 
`/challenge/dont_run` must be killed before `/challenge/run` is executed so that the flag can be obtained 
The PID of `/challenge/dont_run` is found by using the ps
The command is as follows : `ps -ef | grep /challenge/dont_run`
The output obtained is : 
```hacker        73      71  0 05:22 ?        00:00:00 /challenge/dont_run```
hacker        93      75  0 05:22 pts/0    00:00:00 grep --color=auto /challenge/dont_run

The next command is as follows : 
` kill 73`
`/challenge/run`

Flag : `pwn.college{8Wk2pw-j9xI0e66Tdtq0S4qVxj8.dJDN4QDLwgTN0czW}`

## INTERRUPTING PROCESSES

When we run `/challenge/run` command ,this is the output obtained :
`I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!`

Hence we use `Ctrl` command and press `c`, which gives us the flag : `pwn.college{0jUTH_pOxrUodvIgHj1PdeaJXoA.dNDN4QDLwgTN0czW}`

## SUSPENDING PROCESSSES

We learned in the previous challenge to interrup the process we can use `Ctrl-c` , processe can be suspended by using `Ctrl-z`
In this challenge , we will first run the command `/challenge/run' which gives us the output :

```I'll only give you the flag if there's already another copy of me running in ```
` this terminal... Let's check!`

`UID          PID    PPID  C STIME TTY          TIME CMD`

`root          82      65  0 05:32 pts/0    00:00:00 bash /challenge/run`

`root          84      82  0 05:32 pts/0    00:00:00 ps -f`

`I don't see a second me!`

`To pass this level, you need to suspend me and launch me again! You can `
`background me with Ctrl-Z or, if you're not ready to do that for whatever `
`reason, just hit Enter and I'll exit!`

Then we use the hotkey `Ctrl-c` and later `Ctrl-z`, then we run `/challenge/run` again to get the flag
Flag : `pwn.college{s9MN8cyYTgJisTFHIvzuQRsTpi3.dVDN4QDLwgTN0czW}`

## RESUMING PROCESSES

As the name of the challenge suggests we us `fg` comamnd to resume the processes that we have suspended 
We first run `/challenge/run` and then suspend it by using the hotkey `Ctrl-Z` and then enter `fg` to resume it to get the flag .
Flag : `pwn.college{gkvZHIUByVyVFdkXSoH9fcwdpPx.dZDN4QDLwgTN0czW}`

## BACKGROUNDING PROCESSES

The flag is only provided if there exists another copy of `/challenge/run` running and not suspended in the terminal. 
We run `bg` command for the same and run `/challenge/run` again after which we get teh flag 
Flag : `pwn.college{IqbfTx4YRKPbEDT8ofpUwZClRdY.ddDN4QDLwgTN0czW}`

## FOREGROUNDING PROCESSES

To pass this challenge we first suspend the process using the `Ctrl-Z` hotkey after which we use `bg` to run it in the baground , then to resume into the foreground process we enter `fg` which will give us the flag 
Flag : `pwn.college{4OzLarps0et2uvuksSvHmAHipK5.dhDN4QDLwgTN0czW}`

## STARTING BAGROUNDING PROCESSES

As the name of the challenge suggests we can directly baground the process by adding `&` to the end of the command propmt 
The command required to get the flag is as follows : `/challenge/run &`
Flag : `pwn.college{UffNiPk-3DkaeexkVw8lsQOP0WZ.dlDN4QDLwgTN0czW}`

## PROCESS EXIT CODES 

First we run `/challenge/get-code` after which run `/challenge/submit-code` with error code (`$?`) as an argument ie `/challenge/submit-code $?`
Flag : `pwn.college{cYx9A7sf8VOy-FwlAU6kLlvHVFK.dljN4UDLwgTN0czW}`













