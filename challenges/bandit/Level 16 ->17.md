
## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos Acceso
bandit16
JQttfApK4SeyHwDlI9SXGR50qclOAil1
## Solucion
```bash
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 18:33 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00013s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.25 seconds
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Cant use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 7BB5A54E4AB25787770262932FD67C51EF572A43B0D21D5CFC25DE6081852DC5
    Session-ID-ctx: 
    Resumption PSK: 6D252BB0C8CE603D3A33BBD02AF962484C260737EA834BD516D90E4CB8EDA8F8171F255E19A0B23B5481D3E1B38EE1C8
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 46 48 1b 58 8d 73 af 0e-6b c6 b7 9c 29 4b 6f 72   FH.X.s..k...)Kor
    0020 - bf 8b 2c a2 62 0b 28 66-5d 98 c8 04 5b 95 89 af   ..,.b.(f]...[...
    0030 - a9 70 aa bf 1f 38 a6 95-51 58 8b 4d 42 30 a0 93   .p...8..QX.MB0..
    0040 - 8f 9d cb cf 24 f2 20 ba-30 63 a6 7b 88 95 4d 09   ....$. .0c.{..M.
    0050 - dc c2 fa 14 44 75 9b 09-96 bb b5 30 55 9a e6 c3   ....Du.....0U...
    0060 - 70 59 92 2d b8 8b d6 cf-78 d7 e0 8b 6b 19 dd 9a   pY.-....x...k...
    0070 - 3d f8 9c 74 c8 eb 0e e0-9d 2b 6f ea 52 31 8b 44   =..t.....+o.R1.D
    0080 - 12 85 33 ef fc 4e c6 19-8a 69 c2 35 09 e6 04 c4   ..3..N...i.5....
    0090 - 0e da b6 0a c8 e3 ca 90-6c 11 ed 64 ad 98 b1 da   ........l..d....
    00a0 - 71 90 1f b5 da e2 11 0f-16 b6 40 0f d3 b5 49 d5   q.........@...I.
    00b0 - e3 42 b7 17 bb cd c6 64-fb 45 19 c2 da 6f 6f 88   .B.....d.E...oo.
    00c0 - 92 58 d9 d6 d4 f0 ad 4d-f4 db 55 61 49 c3 a6 97   .X.....M..UaI...

    Start Time: 1677177260
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: D82D4343A3B2097EEB1DEBDA96B942ECDCAE85264DCD430CD1D37CAF9B409C9B
    Session-ID-ctx: 
    Resumption PSK: 470A2F5CA110016CEF1AA8B24D0435C1369AF64DF4C670C624894689086687736BF007D243258C84755E51C03AD7E52F
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 49 95 dd e7 0a bf 1c 23-3a 71 9e 5f 3d 13 64 cb   I......#:q._=.d.
    0020 - 89 45 81 87 4c 20 46 a9-83 ca b9 23 b3 4e a0 ab   .E..L F....#.N..
    0030 - b8 79 0a ab 1d b4 99 dd-82 53 d9 c2 6b 66 a3 15   .y.......S..kf..
    0040 - f3 ad 45 50 3f 4b c4 3b-36 07 5c 21 e1 bc c2 c0   ..EP?K.;6.\!....
    0050 - 33 29 f1 a2 80 df 12 ad-a6 f8 95 db c1 6a 9f 23   3)...........j.#
    0060 - 41 56 a3 9e af 44 8e 09-a8 e7 e7 29 4d 66 eb ac   AV...D.....)Mf..
    0070 - ff 2b 9a 8f cb 47 c9 d9-d8 dd 59 2b 10 82 36 7e   .+...G....Y+..6~
    0080 - 9f 5d 7c 98 d2 53 2f 2f-7f 75 9a a7 80 7a 4c 16   .]|..S//.u...zL.
    0090 - 9a 9a 50 a9 a2 80 11 f2-36 f1 95 c9 76 59 d2 1a   ..P.....6...vY..
    00a0 - 95 da c4 56 a6 56 e1 28-0f 8d 4e 96 59 9e 03 0a   ...V.V.(..N.Y...
    00b0 - 70 2a a4 eb 32 88 15 e7-3c d6 f3 ec 15 75 9c c5   p*..2...<....u..
    00c0 - e3 5c 38 b6 2d 23 0f ad-f8 ec 8b e8 60 39 3b 91   .\8.-#......`9;.

    Start Time: 1677177260
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed

┌──(alexia㉿kali)-[/home/alexia]
└─PS> ssh -i llave.txt bandit17@bandit.labs.overthewire.org -p 2220
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e


```
## Notas adicionales
| comando |  descripcion|
|---|----|
|nmap|maps,audits and security scans of networks|


## Referencias



