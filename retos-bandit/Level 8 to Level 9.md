# Level 8 to Level 9

## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit8
Password: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit8@bandit:~$ ls -la
total 56
drwxr-xr-x  2 root    root     4096 Jan 11 19:19 .
drwxr-xr-x 70 root    root     4096 Jan 11 19:19 ..
-rw-r--r--  1 root    root      220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root    root     3771 Jan  6  2022 .bashrc
-rw-r-----  1 bandit9 bandit8 33033 Jan 11 19:19 data.txt
-rw-r--r--  1 root    root      807 Jan  6  2022 .profile
bandit8@bandit:~$ man uniq
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Notas adicionales
| comando | descripción | 
|----------|-------------|
| sort | Ordena líneas de texto |
| uniq | Reporta u omite líneas repetidas |
| -u | Opción para sólo mostrar los únicos |
| -c | Opción para contar las repeticiones de cada línea |
| -d | Opción para mostrar sólo las líneas repetidas |


## Referencias

