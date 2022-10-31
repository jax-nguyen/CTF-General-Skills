# NICE NETCAT
Tags: picoCTF 2021, General Skills  
AUTHOR: SYREAL

## Description:
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...

## Hints:
1. Use `netcat` command
2. Use ASCII language

## Approach:
Use `netcat` command to connect to port 35652 at `mercury.picoctf.net`. It will then return a list of decimal number. We will need to convert those number to text in ASCII to get the flag.

## Solutions:
### Option 1: Manual convert from decimal to ASCII.  
1. Connect to port 35652 at `mercury.picoctf.net`  
`$ nc mercury.picoctf.net 35652`  
it will returns a list of decimal numbers as below  
> 112 105 99 111 67 84 70 123 103 48 48 100 95 107 49 116 116 121 33 95 110 49 99 51 95 107 49 116 116 121 33 95 57 98 51 98 55 51 57 50 125 10  
2. Input the decimal numbers and convert them to ASCII using an online converter like [this one]([url](https://onlineasciitools.com/convert-decimal-to-ascii))
It will convert the numbers to text and we will get the flag  
![Screen Shot 2022-10-31 at 9 35 36 pm](https://user-images.githubusercontent.com/116890436/198990050-058e88f9-4321-4c01-be3f-45ae66a482f6.png)


### Option 2: Automatic convert the numbers from decimal to hexadecimal; and then from hexadecimal to ASCII.

1. Connect to port 35652 at `mercury.picoctf.net`  
`$ nc mercury.picoctf.net 35652`
2. Use the `$ echo` command to export the numbers into standard output  
`$ echo | nc mercury.picoctf.net 35652`
3. Use the `bc` syntax to convert decimal to hexadecimal. [Instruction here](https://www.cyberciti.biz/faq/bc-convert-octal-to-hexadecimal-number/)  
> **Convert dec to hexa:**  
> `echo "obase=16; ibase=10; decimal-number-here" | bc`  
> **Example:**  
> `echo "obase=16; ibase=10; 112" | bc`  
> Where:  
> * obase = Set output base (like 2, 8, 10, 16)
> * ibase = Set input base (like 2, 8, 10, 16)
> * 112 = input number in ibase which to be converted to obase

4. Use the `$ xxd` command to convert from hexadecimal to ASCII  
`$xxd -r -p`

5. We can combine steps 2, 3 & 4 in 1 command line as below:  
`$ (echo "obase=16; ibase=10"; echo | nc mercury.picoctf.net 35652) | bc | xxd -r -p`  
It will return the flag  
![Screen Shot 2022-10-31 at 10 00 25 pm](https://user-images.githubusercontent.com/116890436/198993246-8655cb97-0863-4dc3-a709-d4a8d292cb96.png)

## Flag:
`picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}`
