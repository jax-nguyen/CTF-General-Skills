# WAVE A FLAG
Tags: picoCTF 2021, General Skills  
AUTHOR: SYREAL

# Description:
Can you invoke help flags for a tool or binary? [This program](warm) has extraordinary helpful information...

# Hints:
1. [This program](warm) only work in the webshell or another Linux computer
2. Make the file executable & run it in Terminal prompt

# File:
1. [warm](warm)

# Solutions:
1. Download the file with `$ wget`
2. Make the file executable  
`$ chmod +x warm`
3. Run the file  
`$ ./warm`  
then we will get this instruction.  
`Hello user! Pass me a -h to learn what I can do!`  
![Screen Shot 2022-10-31 at 7 20 16 pm](https://user-images.githubusercontent.com/116890436/198963545-b5dbb5c6-af42-46d1-ab86-8aa68b40d0eb.png)

4. Run the file again with `-h` argument and it will return with the flag.  
`$ ./warm -h`  
![Screen Shot 2022-10-31 at 7 20 29 pm](https://user-images.githubusercontent.com/116890436/198963477-0a7857e7-3058-42d7-8469-831d829e8b6d.png)

# Flag:
`picoCTF{b1scu1ts_4nd_gr4vy_30e77291}`
