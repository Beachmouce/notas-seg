# Level 5 to Level 6

## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

## Datos de acceso al nivel
Host: bandit.labs.overthewire.org  
Port: 2220
Username: bandit5
Password: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

## Solución
```bash
bandit5@bandit:~$ whoami
bandit5
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ ls -R
.:
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17

./maybehere00:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
...

bandit5@bandit:~/inhere$ man find
bandit5@bandit:~/inhere$ find -readable -size 1033c -type f
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```

## Notas adicionales
#### Find
| elemento | descripción | 
|----------|-------------|
| find | Comando para buscar archivos en el sistema |
| -readable | Opción para limitar búsqueda a archivos legibles |
| -size | Opción para limitar búsqueda a archivos con cierto tamaño |
| -type | Opción para especificar el tipo de archivo |

#### Man
| elemento | descripción | 
|----------|-------------|
| man | Comando para pedir el manual de otro comando |
| / | Buscar texto en el manual |
| N | Buscar la siguiente coincidencia hacia atrás |
| n | Buscar la siguiente coincidencia hacia adelante |
| h | Pedir ayuda |
| q | Salir del manual de ayuda |

## Referencias

