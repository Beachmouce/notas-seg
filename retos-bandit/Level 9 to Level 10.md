# Level 9 to Level 10

## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit9
Password: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit9@bandit:~$ ls -la
total 40
drwxr-xr-x  2 root     root     4096 Jan 11 19:18 .
drwxr-xr-x 70 root     root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root     root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit10 bandit9 19379 Jan 11 19:18 data.txt
-rw-r--r--  1 root     root      807 Jan  6  2022 .profile
bandit9@bandit:~$ strings data.txt -n 10 | grep "=="
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Notas adicionales
| elemento | descripción | 
|----------|-------------|
| strings | Imprime las secuencias de caracteres legibles contenidas en un archivo |
| -n 10 | Opción para sólo mostrar las cadenas de tamaño 10 |
| \| | Operador para enviar la salida de un comando a la entrada de otro  |
| grep | Comando para buscar cadenas de texto |

## Referencias

