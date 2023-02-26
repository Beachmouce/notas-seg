# Level 14 to Level 15

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit14
Password: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
ssh -i llave_RSA_14.txt bandit14@bandit.labs.overthewire.org -p 2220

ssh bandit14@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

^C
bandit14@bandit:~$
```

## Notas adicionales


## Referencias

