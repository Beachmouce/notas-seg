# PW Crack 2

## Descripción
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/17/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level2.flag.txt.enc) in the same directory too.

## Hints


## Solución
Al descargar ambos archivos e inspeccionar el código fuente del programa .py, nos damos cuenta que checa si la entrada es igual a la cadena `chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)`. Para averiguar a qué caracteres ASCII corresponde podemos convertirlos a mano o introducirlos en el un shell de python.
```
ttktv-picoctf@webshell:[~/pwc1]: cat level2.py 
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
....
def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")

level_2_pw_check()

ttktv-picoctf@webshell:[~/pwc1]: python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
'4ec9'

ttktv-picoctf@webshell:[~/pwc1]: python level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```

## Bandera 
```
picoCTF{tr45h_51ng1ng_9701e681}
```

## Notas adicionales


## Referencias

