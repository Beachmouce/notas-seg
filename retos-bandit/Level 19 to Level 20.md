# Level 19 to Level 20

## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit19
Password: awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```bash
ssh bandit19@bandit.labs.overthewire.org -p 2220
```


## Solución
```
bandit19@bandit:~$ ./bandit20-do whoami
bandit20
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT

```

## Notas adicionales


## Referencias

