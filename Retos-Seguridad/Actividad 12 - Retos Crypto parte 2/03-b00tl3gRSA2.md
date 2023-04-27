# b00tl3gRSA2

## Descripcion
In RSA d is a lot bigger than e, why don't we use d to encrypt instead of e? Connect with `nc jupiter.challenges.picoctf.org 57464`.

## Pistas
What is e generally?

## Solucion 
```bash
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ python
Python 3.10.8 (main, Nov  4 2022, 09:21:25) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> e=65537
>>> n=94213579262077826836760125170122621905643997878686380300595857634707253871255843052085949075902022884829105470230437362857078358223417973185759648659144380960155014040975658730448943384873055609615711791683583806520611585631288867622270427217235706070534019661373538930120340418894681932991986702610007257029
>>> 
>>> c=7218240386737829143955901201277497590769702422553790837295700681488793098951678160928351090969016665236673426898746634598634391918441999947475402793875830442684454526885446267631679957944362788917706968276238156978789978174263510465590699914132135444493068047831457214208137084873339478223909364076610327382
>>> pow(c,e,n)
180638594769037903267909311328535969949661653320322151351464061
>>> m=pow(c,e,n)
>>> long_to_bytes(m)
b'picoCTF{bad_1d3a5_2152720}'

```
## Bandera
picoCTF{bad_1d3a5_2152720}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|xx|xx|