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
![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2013%20-%20Retos%20Crypto%20parte%203/Pasted%20image%2020230426215352.png)
![[Pasted image 20230426215352.png]]
## Bandera
picoCTF{atbash_crack_92533667}


## Notas Adicionales 
|comando|descripcion|
|---|---|
|xx|xx|
