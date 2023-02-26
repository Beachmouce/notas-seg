# Level 15 to Level 16

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit15
Password: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220
```

## Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
...
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
```

## Notas adicionales


## Referencias
https://en.wikipedia.org/wiki/OpenSSL
