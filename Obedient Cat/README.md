# OBEDIENT CAT
Tags: picoCTF 2021, General Skills.  
AUTHOR: SYREAL

## Description:
This file has a flag in plain sight (aka "in-the-clear").  
[Download flag.](https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag)

## Hints:
1. Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... Everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2. To get the file accessible in your shell, enter the following in the Terminal prompt:  
`$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag`
4. `$ man cat`

## Solution:
1. Download the flag with command:  
`$ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag`
<img width="697" alt="Screen Shot 2022-10-31 at 12 37 23 am" src="https://user-images.githubusercontent.com/116890436/198881531-c88bdb05-c38d-445d-865d-f981641b647a.png">

2. Check the downloaded file in folder with `ls` command  
`$ ls`
<img width="535" alt="Screen Shot 2022-10-31 at 12 31 21 am" src="https://user-images.githubusercontent.com/116890436/198881425-d1cb7a62-e97c-48c5-a728-708b74beeda8.png">

3. Print the flag file with `cat` command:  
`$ cat flag`  
<img width="571" alt="Screen Shot 2022-10-31 at 12 31 48 am" src="https://user-images.githubusercontent.com/116890436/198881434-40fe6930-1338-48b6-8d77-3b824d4ef758.png">

## FLAG
picoCTF{s4n1ty_v3r1f13d_2aa22101}

