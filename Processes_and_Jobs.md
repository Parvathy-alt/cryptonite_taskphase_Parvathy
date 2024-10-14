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




