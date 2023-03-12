# JaWT Scratchpad

## Descripcion
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864

## Pistas
What is that cookie?

Have you heard of JWT?

## Solucion 
```bash
┌──(alexia㉿kali)-[~]
└─$ john
Created directory: /home/alexia/.john
John the Ripper 1.9.0-jumbo-1+bleeding-aec1328d6c 2021-11-02 10:45:52 +0100 OMP [linux-gnu 64-bit x86_64 AVX2 AC]
Copyright (c) 1996-2021 by Solar Designer and others
Homepage: https://www.openwall.com/john/

Usage: john [OPTIONS] [PASSWORD-FILES]

Use --help to list all available options.

                                                                            
┌──(alexia㉿kali)-[~]
└─$ nano hash                   
                                                                        
                                                                            
┌──(alexia㉿kali)-[~]
└─$ ls /usr/share/wordlists
amass      fasttrack.txt  legion      rockyou.txt.gz  wifite.txt
dirb       fern-wifi      metasploit  sqlmap.txt
dirbuster  john.lst       nmap.lst    wfuzz
                                                                            
                                                  
┌──(alexia㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz
[sudo] password for alexia: 
                                                                            
┌──(alexia㉿kali)-[~]
└─$ ls /usr/share/wordlists                         
amass      fasttrack.txt  legion      rockyou.txt  wifite.txt
dirb       fern-wifi      metasploit  sqlmap.txt
dirbuster  john.lst       nmap.lst    wfuzz
                                                                            
┌──(alexia㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123
                                                                            
┌──(alexia㉿kali)-[~]
└─$ john hash -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:04 DONE (2023-03-11 21:30) 0.2136g/s 1580Kp/s 1580Kc/s 1580KC/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
                                                                            
┌──(alexia㉿kali)-[~]
└─$ 

```
![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2006-%20Retos%20web%20parte%202/Pasted%20image%2020230311213412.png)
![[Pasted image 20230311213412.png]]

![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2006-%20Retos%20web%20parte%202/Pasted%20image%2020230311213655.png)
![[Pasted image 20230311213655.png]]


## Bandera
picoCTF{jawt_was_just_what_you_thought_1ca14548}

## Notas Adicionales 
https://jwt.io/

