# fixme2.py

## Descripción
Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/67/fixme2.py)

## Hints


## Solución
Una vez descargado y ejecutado el programa, nos damos cuenta que tiene un error en el código.
Tiene un operador de asignación en lugar de igualación.
```
ttktv-picoctf@webshell:[~/2022]: python fixme2.py 
  File "/home/ttktv-picoctf/2022/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
ttktv-picoctf@webshell:[~/2022]: vim fixme2.py 
ttktv-picoctf@webshell:[~/2022]: python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## Bandera 
```
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## Notas adicionales


## Referencias

