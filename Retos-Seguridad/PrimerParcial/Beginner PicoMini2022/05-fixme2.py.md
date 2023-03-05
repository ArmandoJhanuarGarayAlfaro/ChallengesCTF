# fixme2.py

## Descripcion
Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/66/fixme2.py)

## Pistas
Are equality and assignment the same symbol?

To view the file in the webshell, do: `$ nano fixme2.py`

To exit `nano`, press Ctrl and x and follow the on-screen prompts.

The `str_xor` function does not need to be reverse engineered for this challenge.

## Solucion 
```bash
┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> nano fixme2.py
```
```python
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_ke>


<) + chr(0x41) + chr(0x09) + chr(0x5f) + chr(0x1f) + chr(0x10) + chr(0x3b) +>

  
flag = str_xor(flag_enc, 'enkidu')

# Check that flag is not empty
if flag == "":
  print('String XOR encountered a problem, quitting.')
else:    
  print('That is correct! Here\'s your flag: ' + flag)
```
```bash
┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}


```
## Bandera
picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|nano|permite modificar un archivo|

