# runme.py

## Descripción
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/86/runme.py)

## Hints
If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget` command in the webshell.

## Solución
Descargar el archivo, cambiarle los permisos y ejecutar el script python

```
ttktv-picoctf@webshell:[~]: wget https://artifacts.picoctf.net/c/86/runme.py
--2023-03-11 22:38:52--  https://artifacts.picoctf.net/c/86/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.120, 108.156.172.42, 108.156.172.6, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.120|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                             100%[====================================================================================================================>]     270  --.-KB/s    in 0s      

2023-03-11 22:38:52 (165 MB/s) - 'runme.py' saved [270/270]
ttktv-picoctf@webshell:[~]: ./runme.py
-bash: ./runme.py: Permission denied
ttktv-picoctf@webshell:[~]: chmod +x runme.py 
ttktv-picoctf@webshell:[~]: ./runme.py
picoCTF{run_s4n1ty_run}
```

## Bandera 
```
picoCTF{run_s4n1ty_run}
```

## Notas adicionales


## Referencias

