# Level 10 to Level 11

## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit10
Password: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit10@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit11 bandit10   69 Jan 11 19:18 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit10@bandit:~$ base64 -d data.txt
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```

## Notas adicionales
Opción -d para decodificar el mensaje, que en este caso es el archivo de texto data.txt

## Referencias
https://en.wikipedia.org/wiki/Base64
