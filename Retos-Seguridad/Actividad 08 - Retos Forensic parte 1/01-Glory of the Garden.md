# Glory of the Garden

## Descripcion
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

## Pistas
What is a hex editor?

## Solucion 
```bash
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ xxd garden.jpg
...
...
00230510: f43e b881 5e30 1060 8030 47d6 bacb 58cb  .>..^0.`.0G...X.
00230520: 1046 07b5 7216 df7e 5ff7 c576 363f ebab  .F..r..~_..v6?..
00230530: b70d 18ce 3ccd 6a7e 6b8d af56 b579 39ca  ....<.j~k..V.y9.
00230540: eeef 53ae 8620 31b8 751f 9514 f7fb cff5  ..S.. 1.u.......
00230550: a2bb bdac 9687 98e4 d3b2 e87f ffd9 4865  ..............He
00230560: 7265 2069 7320 6120 666c 6167 2022 7069  re is a flag "pi
00230570: 636f 4354 467b 6d6f 7265 5f74 6861 6e5f  coCTF{more_than_
00230580: 6d33 3374 735f 7468 655f 3379 3333 6464  m33ts_the_3y33dd
00230590: 3265 4546 357d 220a                      2eEF5}".

```
## Bandera
picoCTF{more_than_m33ts_the_3y33dd2eEF5}

## Notas Adicionales 
|comando|descripcion|
|---|---|
|xxd| creates a hex dump of a given file or standard input.|
