# Wave a flag
## Descripcion
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...

## Pistas
This program will only work in the webshell or another Linux computer.

To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm`

Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`

-h and --help are the most common arguments to give to programs to get more information from them!

Not every program implements help features like -h and --help.
## Solucion 
```bash
──(alexia㉿kali)-[~/Downloads]
└─$ ls
file  flag  flag.1  strings  warm
                                                                            
┌──(alexia㉿kali)-[~/Downloads]
└─$ chmod +x warm                                              
                                                                            
┌──(alexia㉿kali)-[~/Downloads]
└─$ ./warm
Hello user! Pass me a -h to learn what I can do!
                                                                            
┌──(alexia㉿kali)-[~/Downloads]
└─$ ./warm -h    
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}


```
## Bandera
picoCTF{b1scu1ts_4nd_gr4vy_755f3544}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|chmod|otorga permisos|
|-h|muestra ayuda|


