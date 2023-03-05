# Tab,Tab,Attack

## Descripcion
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/659efd595171e4c40378be6a2e9b7298/Addadshashanammu.zip)


## Pistas
After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...

## Solucion 
```bash

┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> unzip ./Addadshashanammu.zip
Archive:  ./Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  

┌──(alexia㉿kali)-[/home/alexia/Downloads]
└─PS> cd ./Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/

┌──(alexia㉿kali)-[/home/alexia/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─PS> ls   
fang-of-haynekhtnamet

┌──(alexia㉿kali)-[/home/alexia/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─PS> file ./fang-of-haynekhtnamet                                          
./fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=e34ce4e4ee2f7ce7fb251c8f5ab036da9882bc55, not stripped

┌──(alexia㉿kali)-[/home/alexia/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]       
└─PS> ./fang-of-haynekhtnamet                                               
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}


```
## Bandera
picoCTF{l3v3l_up!_t4k3_4_r35t!_524e3dc4}


## Notas Adicionales 
|comando|descripcion|
|---|---|
|unzip|descomprime un archivo zip|
|file|Muestra el tipo de archivo|

