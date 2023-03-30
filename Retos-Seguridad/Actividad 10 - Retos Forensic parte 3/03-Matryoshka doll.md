# Matryoshka doll
## Descripcion
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/5ef2e9103d55972d975437f68175b9ab/dolls.jpg)

## Pistas
Wait, you can hide files inside files? But how do you find them?
Make sure to submit the flag as picoCTF{XXXXX}
## Solucion 
```bash
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ ls                  
 cliente-main.zip         gestor-de-datos-master.zip
 dolls.jpg                star-admin2-free-admin-template-main
 frameworks2023-master   'star-admin2-free-admin-template-main (1)'
 gestor-de-datos-master
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ open dolls.jpg 
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ file dolls.jpg    
dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg                                                                           
┌──(alexia㉿alexHM)-[~/Downloads]
└─$ cd base_images 
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images]
└─$ ls
2_c.jpg
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images]
└─$ open 2_c.jpg  
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images]
└─$ unzip 2_c.jpg  
Archive:  2_c.jpg
warning [2_c.jpg]:  187707 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/3_c.jpg     
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images]
└─$ cd base_images 
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images/base_images]
└─$ unzip 3_c.jpg 
Archive:  3_c.jpg
warning [3_c.jpg]:  123606 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/4_c.jpg     
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images/base_images]
└─$ cd base_images
                                                                                
┌──(alexia㉿alexHM)-[~/Downloads/base_images/base_images/base_images]
└─$ unzip 4_c.jpg 
Archive:  4_c.jpg
warning [4_c.jpg]:  79578 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: flag.txt                                                                                            
┌──(alexia㉿alexHM)-[~/Downloads/base_images/base_images/base_images]
└─$ cat flag.txt    
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}

```
## Bandera
picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}
## Notas Adicionales 

