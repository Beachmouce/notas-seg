# Level 1 to Level 2

## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit1
Password: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```


## Solución
```bash
bandit1@bandit:~$ whoami
bandit1
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```

## Notas adicionales
El guión se utiliza para pasar argumentos a un comando. Cuando se ejecuta ``` cat - ``` se observa un comportamiento inesperado.

## Referencias
- [Archivos con guiones](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)



