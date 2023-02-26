# Level 20 to Level 21

## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit20
Password: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```bash
ssh bandit20@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit20@bandit:~$ nc -lnvp 3333 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 2841165
bandit20@bandit:~$ Listening on 0.0.0.0 3333

bandit20@bandit:~$ ./suconnect 3333
Connection received on 127.0.0.1 46638
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
[1]+  Done                    nc -lnvp 3333 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$
```

## Notas adicionales
Inicialmente, se configura el puerto 3333 en estado de escuchar, y el operador <<< asigna la contraseña del nivel actual como entrada.

El programa suconnect se ejecuta con el puerto 3333, éste programa lee la contraseña proveída a ese puerto. Confirma que es correcta y responde con la contraseña del siguiente nivel.

## Referencias
https://stackoverflow.com/questions/7950268/what-does-the-bash-operator-i-e-triple-less-than-sign-mean
