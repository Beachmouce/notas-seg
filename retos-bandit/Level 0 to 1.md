# Level 0 to 1

## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit0
Password: bandit0
ssh bandit0@bandit.labs.overthewire.org -p 2220

## Solución
``` bash
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

```



## Notas adicionales
| comando | descripción |
|---------|-------------|
| ls | lista los archivos
| cat | muestra el contenido de un archivo
| pwd | muestra el directorio actual
| clear | borrar la pantalla ó ctrl + L
| whoami | muestra el usuario actual



## Referencias

