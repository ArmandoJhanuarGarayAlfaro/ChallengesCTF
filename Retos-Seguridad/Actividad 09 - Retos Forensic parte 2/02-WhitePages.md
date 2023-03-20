# WhitePages

## Descripcion
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!

## Pistas
(None)

## Solucion 
```bash
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ python extractwhite.py

		picoCTF

		SEE PUBLIC RECORDS & BACKGROUND REPORT
		5000 Forbes Ave, Pittsburgh, PA 15213
		picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}
		

$ cat extractwhite.py                           
def convertSpacesToBinary():
    with open('whitepages.txt', 'rb') as f:
        result = f.read()
        result = result.replace(b'\xe2\x80\x83', b'0')
        result = result.replace(b'\x20', b'1')
        result = result.decode()
    return result    

def convertFromBinaryToASCII(binaryValues):

    binary_int = int(binaryValues, 2)
    byte_number = binary_int.bit_length() + 7 // 8

    binary_array = binary_int.to_bytes(byte_number, "big")
    ascii_text = binary_array.decode('ascii')

    print(ascii_text)

convertFromBinaryToASCII(convertSpacesToBinary())    
```
## Bandera
picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}

## Notas Adicionales 

