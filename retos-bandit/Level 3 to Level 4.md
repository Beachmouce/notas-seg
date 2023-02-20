# Level 3 to Level 4

## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit3
Password: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

## Solución
```
bandit3@bandit:~$ whoami
bandit3
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jan 11 19:19 .
drwxr-xr-x 3 root    root    4096 Jan 11 19:19 ..
-rw-r----- 1 bandit4 bandit3   33 Jan 11 19:19 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```

## Notas adicionales


## Referencias

