# HideToSee

## Descripcion
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/235/atbash.jpg).

## Pistas
Download the image and try to extract it.

## Solucion 
```bash
──(alexia㉿alexHM)-[~/Downloads]
└─$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ cat encrypted.txt  
krxlXGU{zgyzhs_xizxp_92533667}


```
![[Pasted image 20230426215352.png]]
## Bandera
picoCTF{atbash_crack_92533667}


## Notas Adicionales 
|comando|descripcion|
|---|---|
|xx|xx|
