# PW Crack 2

## Descripcion
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/16/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level2.flag.txt.enc) in the same directory too.
## Pistas
Does that encoding look familiar?

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion 
```bash

┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> cat ./level2.py
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()
```

```python
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36) 
'de76'
```

```bash
┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> python ./level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```


## Bandera
picoCTF{tr45h_51ng1ng_489dea9a}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|cat|Muestra el contenido de un archivo|
|chr|Permite visualizar y modificar archivos|

