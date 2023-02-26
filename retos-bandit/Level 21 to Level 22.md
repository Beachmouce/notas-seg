# Level 21 to Level 22

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit21
Password: NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
```bash
ssh bandit21@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit21@bandit:~$ ls -la /etc/cron.d/cronjob_bandit22
-rw-r--r-- 1 root root 120 Feb 21 22:03 /etc/cron.d/cronjob_bandit22
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
```

## Notas adicionales
Notamos que el trabajo cronjob_bandit22 ejecuta el script cronjob_bandit22.sh periódicamente. Usamos cat para ver qué hace ese script y al analizarlo, nos damos cuenta que almacena la bandera del siguiente nivel (del archivo al que no debemos tener acceso) y la almacena en un archivo temporal, al que sí tenemos acceso.

## Referencias
https://es.wikipedia.org/wiki/Cron_(Unix)
