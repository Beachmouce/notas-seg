# PW Crack 3

## Descripción
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/24/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/24/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/24/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Hints


## Solución
Descargar los 3 archivos y examinar el código fuente del programa python.
En una lista al final del programa se encuentra la lista de contraseñas posibles para que nos de acceso a la bandera

```
ttktv-picoctf@webshell:[~/pw3]: ls
level3.flag.txt.enc  level3.hash.bin  level3.py
ttktv-picoctf@webshell:[~/pw3]: cat level3.py
import hashlib

### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    
...

# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

ttktv-picoctf@webshell:[~/pw3]: python level3.py 
Please enter correct password for flag: f09e
That password is incorrect
ttktv-picoctf@webshell:[~/pw3]: python level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
ttktv-picoctf@webshell:[~/pw3]: python level3.py 
Please enter correct password for flag: 87ab
That password is incorrect
ttktv-picoctf@webshell:[~/pw3]: python level3.py 
Please enter correct password for flag: dba8
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

## Bandera 
```
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

## Notas adicionales


## Referencias

