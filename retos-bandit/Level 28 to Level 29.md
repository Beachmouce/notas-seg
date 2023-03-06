# Level 28 to Level 29

## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit28
Password: AVanL161y9rsbcJIsFHuw35rjaOM19nR
```bash
ssh bandit28@bandit.labs.overthewire.org -p 2220
```


## Solución
Se clona el repositorio alojado en el puerto 2220. Al revisar su contenido, nos damos cuenta que contiene el texto `username: bandit29 password: xxxxxxxxxx`  lo cual podría significar que anteriormente había una contraseña que fue puesta ahí accidentalmente que fue reemplazada por 'x' después. Se revisan los logs y se utiliza el comando `git checkout` para regresar a un commit anterior

```
bandit28@bandit:/tmp/sfsf1515$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit28/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit28-git@localhost's password:
remote: Enumerating objects: 9, done.
...
...
drwxrwxr-x    3 bandit28 bandit28   4096 Mar  6 01:41 repo
bandit28@bandit:/tmp/sfsf1515$ cd repo
bandit28@bandit:/tmp/sfsf1515/repo$ ls -la
total 16
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  6 01:41 .
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  6 01:41 ..
drwxrwxr-x 8 bandit28 bandit28 4096 Mar  6 01:41 .git
-rw-rw-r-- 1 bandit28 bandit28  111 Mar  6 01:41 README.md
bandit28@bandit:/tmp/sfsf1515/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx

bandit28@bandit:/tmp/sfsf1515/repo$ git log
commit 104db85a904e9691ff22aafe1a96124c88f75afa (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    fix info leak

commit 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Author: Morla Porla <morla@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    add missing data

commit cd3b97ef95879ec34df0d6c82f2a96d552f0e56c
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:10 2023 +0000

    initial commit of README.md
bandit28@bandit:/tmp/sfsf1515/repo$ git checkout 6c3c5e485cc531e5d52c321587ce1103833ab7c3
Note: switching to '6c3c5e485cc531e5d52c321587ce1103833ab7c3'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6c3c5e4 add missing data
bandit28@bandit:/tmp/sfsf1515/repo$ ls -la
total 16
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  6 01:43 .
drwxrwxr-x 3 bandit28 bandit28 4096 Mar  6 01:41 ..
drwxrwxr-x 8 bandit28 bandit28 4096 Mar  6 01:43 .git
-rw-rw-r-- 1 bandit28 bandit28  133 Mar  6 01:43 README.md
bandit28@bandit:/tmp/sfsf1515/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```

## Notas adicionales


## Referencias
[Git checkout](https://www.gitkraken.com/learn/git/problems/git-checkout-commit)