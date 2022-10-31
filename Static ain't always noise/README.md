# STATIC AIN'T ALWAYS NOISE
Tags: picoCTF 2021, General Skills  
AUTHOR: SYREAL  
Points: 20

# Description:
> Can you look at the data in this binary: [static](static)? This [BASH script](ltdis.sh) might help!

# File:
1. [static](static)
2. [ltdis.sh](ltdis.sh)

# Solution:
1. Download all files with `$ wget`
2. Make the files executable  
`$ chmod +x static`  
`$ chmod +x ltdis.sh`
3. Run [static](static) file and see what's in there  
`$ ./static`  
The file returns with a hint  
> Oh hai! Wait what? A flag? Yes, it's around here somewhere!  

From the hint, we know that the flag is in the [static](static) file

4. Run the [Bash script](ltdis.sh)  
`$ ./ltdis.sh`  
And it will returns this
```
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
```
From the usage, we know that we need to run the [Bash script](ltdis.sh) on a file which is the [static](static) file  
`$ ./ltdis.sh static`  
After that, we got this result  
```
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
```
From the above message, we know that all the strings found in [static](static) file has been written to static.ltdis.strings.txt. Since the flag is also a string of random characters, it should also be in that file  

5. We know that the flag is a string starts with "picoCTF". We can find the flag in strings file using the `$ grep` command and it will return with the flag    
`$ grep picoCTF static.ltdis.strings.txt`  
Results:  
> 1020 picoCTF{d15a5m_t34s3r_f6c48608}

# Flags:
> picoCTF{d15a5m_t34s3r_f6c48608}
