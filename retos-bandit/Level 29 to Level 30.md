# Level 29 to Level 30

## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit29
Password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```bash
ssh bandit29@bandit.labs.overthewire.org -p 2220
```



## Solución
Al examinar el archivo README.md nos dan una pista que dice que no hay passwords en la rama de producción, por lo que deberíamos cambiar a otras ramas para ver qué hay.
```
bandit29@bandit:/tmp/temporal229$ ls -la
total 124
drwxrwxr-x    3 bandit29 bandit29   4096 Mar  6 01:50 .
drwxrwx-wt 1187 root     root     114688 Mar  6 01:50 ..
drwxrwxr-x    3 bandit29 bandit29   4096 Mar  6 01:50 repo
bandit29@bandit:/tmp/temporal229$ cd repo
bandit29@bandit:/tmp/temporal229/repo$ ls -la
total 16
drwxrwxr-x 3 bandit29 bandit29 4096 Mar  6 01:50 .
drwxrwxr-x 3 bandit29 bandit29 4096 Mar  6 01:50 ..
drwxrwxr-x 8 bandit29 bandit29 4096 Mar  6 01:50 .git
-rw-rw-r-- 1 bandit29 bandit29  131 Mar  6 01:50 README.md
bandit29@bandit:/tmp/temporal229/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>


bandit29@bandit:/tmp/temporal229/repo$ git branch -r
  origin/HEAD -> origin/master
  origin/dev
  origin/master
  origin/sploits-dev

bandit29@bandit:/tmp/temporal229/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/temporal229/repo$ cat README.md
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```

## Notas adicionales
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

## Referencias

