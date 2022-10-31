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
2. View the password from [pw.txt](pw.txt) file with `$ cat` command
3. View the Python Script with `$ nano` command
4. Run the Python script with`$ python` command
