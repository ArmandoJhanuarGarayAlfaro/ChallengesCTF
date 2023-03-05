int# Lets Warm Up

## Descripcion
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Pistas
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

## Solucion 
```bash
greengoalexh-picoctf@webshell:~$ python
```
```python
>>> int(0x70)
112
>>> chr(112)
'p'
```
`
## Bandera
picoCTF{p}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|int|Transforma a numero entero|
|chr|Transforma un numero a una letra|


