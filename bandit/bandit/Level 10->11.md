
## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos Acceso
bandit10
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Solucion
```bash
bandit10@bandit:~$ ls 
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ echo "mensaje secreto" | base64
bWVuc2FqZSBzZWNyZXRvCg==
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ cat data.txt |base64
VkdobElIQmhjM04zYjNKa0lHbHpJRFo2VUdWNmFVeGtVakpTUzA1a1RsbEdUbUkyYmxaRFMzcHdh
R3hZU0VKTkNnPT0K
bandit10@bandit:~$ cat data.txt |base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$ 



```
## Notas adicionales
| comando |  descripcion|
|---|----|
|Base 64 | sirve para decodificar o codificar|



## Referencias



