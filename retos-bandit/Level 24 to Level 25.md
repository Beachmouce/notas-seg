# Level 24 to Level 25

## Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit24
Password: VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```bash
ssh bandit24@bandit.labs.overthewire.org -p 2220
```


## Solución
Se crea un mini-script plasmado en una sola línea que genera líneas de texto con la plantilla "``VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i``", donde $i representa un pin numérico de 4 digitos que va desde 0000 a 9999 según la estructura  ``for`` declarada. Cada una de estas líneas se le envía al puerto 30002 del localhost, el cual responderá con la flag del siguiente nivel cuando el pin generado sea el correcto. La salida de este comando se manda al comando ``grep ``con la opción ``-v``, la cual invierte la búsqueda de manera sólo regresa líneas que NO contengan la palabra Wrong. Esto para obtener la respuesta sin los mensajes de error.
```
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v Wrong
I am the pincode checker for user bandit25. Please enter the password for user bandit24 and the secret pincode on a single line, separated by a space.
Correct!
The password of user bandit25 is p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d

Exiting.
```

## Notas adicionales


## Referencias

