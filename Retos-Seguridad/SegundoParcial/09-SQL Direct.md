# SQL Direct

## Descripcion
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.

Connect to this PostgreSQL server and find the flag! `psql -h saturn.picoctf.net -p 50859 -U postgres pico` Password is `postgres`
## Pistas
What does a SQL database contain?
## Solucion 
```bash
┌──(alexia㉿alexHM)-[~/Documents/SextoSemestre]
└─$ psql -h saturn.picoctf.net -p 50859 -U postgres pico
Password for user postgres: 
psql (15.2 (Debian 15.2-2))
Type "help" for help.

pico=# \c pico
You are now connected to database "pico" as user "postgres".
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags
pico-# ;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

pico=# 



```
## Bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|xx|xx|
