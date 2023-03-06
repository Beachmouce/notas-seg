# Level 31 to Level 32

## Objetivo
There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit31
Password: OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```bash
ssh bandit31@bandit.labs.overthewire.org -p 2220
```


## Solución
El archivo README.md dice que ahora debemos crear un archivo llamado ``key.txt`` que contenga la frase ``'May I come in?'`` sin comillas. Creamos ese archivo con un editor de texto, realizamos el commit y push y nos proporcionan la llave para el siguiente nivel.

```
bandit31@bandit:/tmp/767676/repo$ vim key.txt
bandit31@bandit:/tmp/767676/repo$ cat key.txt
May I come in?

bandit31@bandit:/tmp/767676/repo$ git add key.txt
The following paths are ignored by one of your .gitignore files:
key.txt
hint: Use -f if you really want to add them.
hint: Turn this message off by running
hint: "git config advice.addIgnoredFile false"

bandit31@bandit:/tmp/767676/repo$ git add -f key.txt
bandit31@bandit:/tmp/767676/repo$ git commit -m "ahora si"
[master 8014c1b] ahora si
 1 file changed, 1 insertion(+), 1 deletion(-)
bandit31@bandit:/tmp/767676/repo$ git push
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit31/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit31-git@localhost's password:
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 2 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (6/6), 531 bytes | 531.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: ### Attempting to validate files... ####
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
remote: Well done! Here is the password for the next level:
remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y
remote:
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.
remote:
```

## Notas adicionales


## Referencias

