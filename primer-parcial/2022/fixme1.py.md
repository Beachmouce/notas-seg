# fixme1.py

## Descripción
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/38/fixme1.py)

## Hints


## Solución
Después de descargar el archivo y ejecutarlo con python, nos damos cuenta que hay un error en el código.
Editamos el archivo para arreglar la indentación y ejecutamos.
```
ttktv-picoctf@webshell:[~/2022]: python fixme1.py 
  File "/home/ttktv-picoctf/2022/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
ttktv-picoctf@webshell:[~/2022]: vim fixme1.py 
ttktv-picoctf@webshell:[~/2022]: python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
```

## Bandera 
```
picoCTF{1nd3nt1ty_cr1515_09ee727a}
```

## Notas adicionales


## Referencias

