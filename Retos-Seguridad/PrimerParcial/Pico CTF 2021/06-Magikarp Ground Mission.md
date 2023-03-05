# Magikarp Ground Mission

## Descripcion
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `6d448c9c`

Additional details will be available after launching your challenge instance.

SSH

`ssh ctf-player@venus.picoctf.net -p 49388`

## Pistas
Finding a cheatsheet for bash would be really helpful!

## Solucion 
```bash
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  dev   instructions-to-3of3.txt  media  proc  sbin  tmp
bin            etc   lib                       mnt    root  srv   usr
boot           home  lib64                     opt    run   sys   var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ ^C
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ 




```
## Bandera
picoCTF{xxsh_0ut_0f_\/\/4t3r_5190b070}


## Notas Adicionales 
|comando|descripcion|
|---|---|
|cat|Muestra el contenido de un archivo|
