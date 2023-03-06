# Level 25 to Level 26

## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit25
Password: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
```bash
ssh bandit25@bandit.labs.overthewire.org -p 2220
```


## Solución
Al analizar los archivos de la carpeta home nos damos cuenta que está presenta la llave ssh para conectarse al nivel 26. Simplemente usarla y continuar.
```
bandit25@bandit:~$ ls -la
total 32
drwxr-xr-x  2 root     root     4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root     4096 Feb 21 22:04 ..
-rw-r-----  1 bandit25 bandit25   33 Feb 21 22:03 .bandit24.password
-r--------  1 bandit25 bandit25 1679 Feb 21 22:03 bandit26.sshkey
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit25 bandit25    4 Feb 21 22:03 .pin
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p 2220


c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```

## Notas adicionales


## Referencias

