
## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos Acceso
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## Solucion
```bash
bandit14@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:56 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:56 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:56 2023 GMT; NotAfter: Feb 21 22:03:56 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEF3vcjDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU2WhcNMjMwMjIxMjIwMzU2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCg
1elREdWTbtCZNl7KNMjleNrcG71f9lZhjAfM4x+TDwlPpT+Q9O3V6J687fJdMH85
xfUwcZG0XFCeN1nxnmQadGF/ZHEt0laWmCQfo5LogzgGFcaZWC1a6XZ5ZKv7SRDt
tvPK/CTKwOJD5ZJVEXEk9R8YQ/VbKwZMDc43WD/HKypvBv7fZVbJkKYY75LOby86
7gux29Emhntj5pZyYagYbmonnAiw6447bGTC1d6jilGPhXMzckTI57WGeNdp4ppL
3pXSVDLOU2XJ8Um/L2VIgGTsUk5CwrtzVxyt6I5sKavUhsNGlzqvHI/McgbsnHi8
3LDg9k/Co8F21eZFooVlAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBz
lgp6XhMshglRxhxHRg1xHkVYSFSBaS5Adq5OIoE/oetyedTiO2B9MLmNZ9Juu/WK
/+WZFmNdzQ6Iw5ueBz/rmY+DvzTjjd4CPPqeilG5mngceR5nliM9mXkpQlmm3T1a
8JuBrDugrN9BP4IeBTER0pgQcQvsRATrv/SAVFVBhTSvOKFhoYNEdBzaqxclEjD6
bl3UkzNag/S3iLuv24xoQkMmlFC2afaswkG/cQ4p3BuapuZORjbohUOXS24QDl0z
A2RDFNizi42ZVJ8ZW1qbURZ4n/VbIAi7vRHldPKjC8hYAcdvUekB0schBlc1J06Z
phGCgzTVUzJu9yz8uKzO
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
    Session-ID: C364BE554C5B390C90457F48244CCB32AC328F144678764F3F35BFA8D225E447
    Session-ID-ctx: 
    Resumption PSK: D5A66DBBC3BEA8331F96BAC062888E3B65940245747057112C9501B748550E5239C0C23AFE00AC1B1C61C172D55AAE42
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - a5 3d 92 1f d1 78 36 48-bb a6 da 4d 19 13 ee a7   .=...x6H...M....
    0010 - a3 f4 78 22 93 2e e2 7f-e6 76 99 c5 8f 74 bd 64   ..x".....v...t.d
    0020 - eb 25 c4 d8 da 01 0c bb-59 26 bf 13 ee e4 62 60   .%......Y&....b`
    0030 - 4c fd 1f 90 4c 62 62 5e-24 6a d9 10 40 9d 50 42   L...Lbb^$j..@.PB
    0040 - 89 a5 4a b9 fb b3 7a 30-02 20 32 5e 7b d5 d1 aa   ..J...z0. 2^{...
    0050 - 4c 64 63 25 21 00 55 f3-1d 02 5d bb b3 17 ef 37   Ldc%!.U...]....7
    0060 - 1b df b1 49 dd 1e 1d b8-a5 c7 77 74 4f be 58 f8   ...I......wtO.X.
    0070 - 3e a3 03 16 ad 33 c9 47-95 36 cc d9 8c 6b 7e 0c   >....3.G.6...k~.
    0080 - 62 24 8b 75 60 65 b2 97-f9 97 2b f5 04 f1 a4 13   b$.u`e....+.....
    0090 - c6 6d ab 9c db 6f a8 31-4e 8f 63 19 44 44 f8 73   .m...o.1N.c.DD.s
    00a0 - 99 97 9a 45 d1 b2 ed 1d-b9 64 fe 19 1f 68 9c d3   ...E.....d...h..
    00b0 - e1 e1 68 52 40 ca 08 12-2d 10 66 87 06 a1 5a 90   ..hR@...-.f...Z.
    00c0 - ac 14 ef d3 19 94 f1 af-4a d8 56 68 7e a1 e1 7a   ........J.Vh~..z

    Start Time: 1677020739
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
    Session-ID: 2F82A4E3A2E37B9FBAFE41CCB7D3713835BC8EC18CBFB5400BC7B88757187226
    Session-ID-ctx: 
    Resumption PSK: 32F2CC3847F517BEA2F6C557DAEDBF2C2A7A38C05A7FC6EF0B0EC60F0587397BEC7ECB8600F646F1EC1E1FC44878CED7
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - a5 3d 92 1f d1 78 36 48-bb a6 da 4d 19 13 ee a7   .=...x6H...M....
    0010 - 74 b5 17 2e c8 75 7a 9d-1b ce 31 82 bf 84 9f 4e   t....uz...1....N
    0020 - b7 06 2f 58 5c de 24 f1-28 01 39 b3 d8 dc e7 e0   ../X\.$.(.9.....
    0030 - 8d c6 92 81 60 e1 3e f6-a1 26 30 24 e3 ef ff b5   ....`.>..&0$....
    0040 - c9 f2 79 d5 c3 d6 2b a3-db 4e 05 60 cb 85 72 09   ..y...+..N.`..r.
    0050 - cf d3 65 99 ae 07 d0 82-04 4e d0 b2 ba 44 05 f5   ..e......N...D..
    0060 - ff d4 d5 b0 07 d3 c7 c4-c0 5b b6 01 a1 c3 ef fd   .........[......
    0070 - be 55 29 a0 20 da f1 dc-e1 a3 2e 0d 2f d3 46 e4   .U). ......./.F.
    0080 - 92 9e cd a1 06 d6 1e 4c-0a 85 2c b6 e3 5d 69 9d   .......L..,..]i.
    0090 - 57 e8 fc 27 54 78 fd e6-7d d0 18 56 9b 6e 1a 46   W..'Tx..}..V.n.F
    00a0 - 90 19 25 46 cd 7b b4 78-e3 f8 27 b6 9e 75 95 68   ..%F.{.x..'..u.h
    00b0 - f9 f0 f4 71 d9 9c 7c 60-d1 f0 10 65 e4 31 85 d4   ...q..|`...e.1..
    00c0 - 6f 74 14 12 fa 03 f6 0d-56 8d 64 80 fb 6c 7b 66   ot......V.d..l{f

    Start Time: 1677020739
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1


```
## Notas adicionales
| comando |  descripcion|
|---|----|
|openssl|commonly used to identufy certificate info|

## Referencias



