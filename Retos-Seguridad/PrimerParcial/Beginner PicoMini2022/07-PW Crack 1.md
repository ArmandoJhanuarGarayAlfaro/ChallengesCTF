# PW Crack 1

## Descripcion
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/53/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/53/level1.flag.txt.enc) in the same directory too.

## Pistas
To view the file in the webshell, do: `$ nano level1.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.
## Solucion 
```bash
┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> nano level1.py

┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> python level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```
## Bandera
picoCTF{545h_r1ng1ng_1b2fd683}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|nano|Permite visualizar y modificar archivos|
