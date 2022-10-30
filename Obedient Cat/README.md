# OBEDIENT CAT
Tags: picoCTF 2021, General Skills
AUTHOR: SYREAL

## DESCRIPTION:
This file has a flag in plain sight (aka "in-the-clear").
[Download flag.](https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag)

## HINTS:
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... Everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
3. $ man cat

## SOLUTION:
1. Download the flag with command:
`$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag`

2. Check if the flag is downloaded in the folder:
`$ ls`

3. Print the flag file with command:
`$ cat flag`

## FLAG
picoCTF{s4n1ty_v3r1f13d_2aa22101}

