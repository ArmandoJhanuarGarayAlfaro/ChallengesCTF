# fixme1.py

## Descripcion
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/37/fixme1.py)

## Pistas
Indentation is very meaningful in Python

To view the file in the webshell, do: `$ nano fixme1.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion 
```bash
┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> nano fixme1.py
```
```python
import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_ke>


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0>

  
flag = str_xor(flag_enc, 'enkidu')
print('That is correct! Here\'s your flag: ' + flag)
```
```bash
┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
## Bandera
picoCTF{1nd3nt1ty_cr1515_6a476c8f}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|nano|Permite modificar un archivo|
