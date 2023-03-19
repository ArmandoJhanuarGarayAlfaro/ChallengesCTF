# extensions

## Descripcion
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?

## Pistas
How do operating systems know what kind of file it is? (It's not just the ending!
Make sure to submit the flag as picoCTF{XXXXX}

## Solucion 
```bash
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ file flag.txt 
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ mv flag.txt flag.png
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ open flag.png    

```

![[Pasted image 20230318210202.png]]
## Bandera
picoCTF{now_you_know_about_extensions}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|xx|xx|
