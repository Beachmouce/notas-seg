# Level 2 to Level 3

## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit2
Password: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

## Solución
```bash
bandit2@bandit:~$ whoami
bandit2
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```

## Notas adicionales


## Referencias

