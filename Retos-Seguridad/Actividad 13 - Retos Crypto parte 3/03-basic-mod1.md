# basic-mod1

## Descripcion
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/129/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Pistas
Do you know what `mod 37` means?

`mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.


## Solucion 
```bash
──(alexia㉿alexHM)-[~/Downloads]
└─$ python run.py
picoCTF{R0UND_N_R0UND_ADD17EC2}


```
```python
numbers="350 63 353 198 114 369 346 184 202 322 94 235 114 110 185 188 225 212 366 374 261 213"

numbers=numbers.split(" ")

modded=[]

for x in numbers:

modded.append(int(x)%37)

translated=""

for x in modded:

if(x == 36):

x="_"

if(x == 0):

x="A"

  

if(x == 1):

x="B"

if(x == 2):

x="C"

if(x == 3):

x="D"

if(x == 4):

x="E"

if(x == 7):

x="H"

if(x == 8):

x="I"

if(x == 11):

x="L"

if(x == 12):

x="M"

if(x == 13):

x="N"

if(x == 15):

x="P"

if(x == 16):

x="Q"

if(x == 17):

x="R"

if(x == 19):

x="T"

if(x == 20):

x="U"

if(x == 25):

x="Z"

if(x == 26):

x="0"

if(x == 27):

x="1"

if(x == 28):

x="2"

if(x == 29):

x="3"

if(x == 30):

x="4"

if(x == 33):

x="7"

  

translated=translated+str(x)

  

print("picoCTF{"+translated+"}")
```
## Bandera
picoCTF{R0UND_N_R0UND_ADD17EC2}


## Notas Adicionales 

