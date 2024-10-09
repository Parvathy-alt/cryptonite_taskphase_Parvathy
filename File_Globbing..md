# FILE GLOBBING

## MATCHING WITH *

## MATCHING WITH ?

When the system comes across a `?` character in any argument, the shell interprets it as a wildcard that matches exactly one character, similar to `*`, but limited to a single character.
On running `cd /?ha??enge ./run` we recive the flag which is : `pwn.college{g2ZYkLXFtVpYu0hlIejBNjDZ3yJ.dJjM4QDLwgTN0czW}`

## MATCHING WITH []

As mentioned in the challenge itself "The square brackes are, essentially, a limited form of '?' " . [] is a wildcard for some subset of potential characters, specified within the brackets. For this challenge we first run ` cd /challenge/files` after which
we execute ` /challenge/run file_[absh] ` to access the file file_b, file_a, file_s, and file_h 
The flag obtained is : `pwn.college{0irKRbuJgGGWQXMI7XDMzk-A436.dNjM4QDLwgTN0czW}`

## MATCHING PATHS WITH []

## MIXING GLOBS

The challenge asks us to first `cd` into `/challenge/files` which prints out words starting with alphabets a to z . 
We are asked to write a single, short (6 characters or less) glob that will match the files "challenging", "educational", and "pwning". 
When the command `/challenge/run [cep]*` is run we get out flag which is : `pwn.college{QwaDrNoOJa53L4kl3G5x4LaT8yr.dVjM4QDLwgTN0czW}`

## EXCLUSIONARY GLOBBING

As the name of the challenge suggests , exclusionary globbing helps us filter out files that are not relevant for our search . 
Adding " ! " or " ^ " inside the [] before the first letter of the file to filter out files that are not needed to be printed . 
First we `cd` to `/challenge/files` later we run `/challenge/run [!pwn]*` command to obtain the flag whiich is : 
`pwn.college{kfORaBNTGZuQQeTJJisOrlq8f0A.dZjM4QDLwgTN0czW}`




