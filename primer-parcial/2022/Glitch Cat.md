# Glitch Cat

## Descripción
Our flag printing service has started glitching! `$ nc saturn.picoctf.net 53933`

## Hints
ASCII is one of the most common encodings used in programming

## Solución
Al conectarnos con netcat se nos presenta una bandera incompleta, donde algunos caracteres están expresados en su representación ASCII hexadecimal. Abrimos el shell de python e introducimos la bandera como cadena de texto. Python interpreta los caracteres hexadecimales y nos arroja la bandera decodificada.

```
ttktv-picoctf@webshell:[~/2022]: nc saturn.picoctf.net 53933
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

ttktv-picoctf@webshell:[~/2022]: python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
'picoCTF{gl17ch_m3_n07_a4392d2e}'
```

## Bandera 
```
picoCTF{gl17ch_m3_n07_a4392d2e}
```

## Notas adicionales


## Referencias

