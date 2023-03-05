# Obediant Cat

## Descripcion
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag).

## Pistas
Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.

To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag`

`$ man cat`

## Solucion 
```bash
┌──(alexia㉿kali)-[~/Downloads]
└─$ cat flag  
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}


```
## Bandera
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|cat|Muestra el contenido del archivo|
