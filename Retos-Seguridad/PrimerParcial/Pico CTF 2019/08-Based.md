# Based

## Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

## Pistas
I hear python can convert things.

It might help to have multiple windows open.


## Solucion 
Se utilizaron los siguientes links de conversion:
https://www.geocachingtoolbox.com/index.php?page=asciiConversion
https://www.rapidtables.com/convert/number/hex-to-ascii.html
```bash
┌──(alexia㉿kali)-[~/Downloads]
└─$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
falcon
Please give me the  143 157 155 160 165 164 145 162 as a word.
Input:
computer
Please give me the 6c616d70 as a word.
Input:
lamp
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}


```
## Bandera
picoCTF{learning_about_converting_values_b375bb16}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|nc|realiza una conexion|
