# PYTHON WRANGLING
Tags: picoCTF 2021, General Skills.  
AUTHOR: SYREAL

## Description:
Python scripts are invoked kind of like programs in the Termnial... Can you run [this Python script](ende.py) using [this password](pw.txt) to get [the flag](flag.txt.en)?

## Hints:
1. Download Python script 
2. `$ man python`

## File:
1. [Python script](ende.py)
2. [Password](pw.txt)
3. [Flag](flag.txt.en)

## Approach:
The flag is encrypted. We would need to get the password from [pw.txt](pw.txt) file, and then run the [Python script](ende.py) to decode the [flag](flag.txt.en) with the obtained password.

## Solutions:
1. Download all files with `$ wget` command
2. View the password from [pw.txt](pw.txt) file with `$ cat` command.  
<img width="316" alt="Screen Shot 2022-10-31 at 6 29 20 pm" src="https://user-images.githubusercontent.com/116890436/198958362-daf9eb5d-da19-41c2-af5d-39a9343730d2.png">
3. View the Python Script with `$ nano` command.  
By examining the Python script, we know that we need to run it with either 1 of 2 argument :-d/-e  
![Screen Shot 2022-10-31 at 6 45 48 pm](https://user-images.githubusercontent.com/116890436/198959895-21bcaa25-756c-4c89-98ea-1853236e7d8c.png)

-d will be for decrypting.  
![Screen Shot 2022-10-31 at 6 45 59 pm](https://user-images.githubusercontent.com/116890436/198959592-93295562-83b9-46f5-b296-dc96572c3fbc.png)

-e will be for encrypting.  
![Screen Shot 2022-10-31 at 6 49 42 pm](https://user-images.githubusercontent.com/116890436/198959632-d065a9dc-035d-4dca-a0d1-af1c906ff286.png)

4. Exit the python script with `Ctrl + X`. Run the Python script to decripted the [flag.txt.en](flag.txt.en) by using `$ python` command with ` -d` argument.  
`$ python ende.py -d flag.txt.en`.  
Enter the password from [pw.txt](pw.txt) file obtained in Step 2 and we will get the flag as below
![Screen Shot 2022-10-31 at 6 55 47 pm](https://user-images.githubusercontent.com/116890436/198959035-4af8f94d-20ee-428b-95d7-23830432fd81.png)

