# shark on wire 2

## Descripcion
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Pistas
(None)

## Solucion 
![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2009%20-%20Retos%20Forensic%20parte%202/Pasted%20image%2020230320160259.png)
![[Pasted image 20230320160259.png]]

```python
>>> chr(112)+chr(105)+chr(99)+chr(111)+chr(67)+chr(84)+chr(70)+chr(123)+chr(112)+chr(49)+chr(76)+chr(76)+chr(102)+chr(51)+chr(114)+chr(51)+chr(100)+chr(95)+chr(100)+chr(97)+chr(116)+chr(97)+chr(95)+chr(118)+chr(49)+chr(97)+chr(95)+chr(115)+chr(116)+chr(51)+chr(103)+chr(48)+chr(125)
'picoCTF{p1LLf3r3d_data_v1a_st3g0}'


```
## Bandera
picoCTF{p1LLf3r3d_data_v1a_st3g0}
## Notas Adicionales 

