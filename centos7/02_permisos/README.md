# Comandos CentOS7

## Comandos comunes

| Comando   | Usuario | Descripción   |
|------|------|------|
| --- | root | Los siguientes comandos se ejcutan como el usuario root |
| # cd /tmp | root | Cambie el path al directorio tmp |
| # touch message_1.txt | root | Cree un archivo de nombre message_1.txt |
| # ls -l message_1.txt | root | Listar las propiedades del archivo message_1.txt |
| # vi message_1.txt | root | Edite el archivo message_1.txt |
| # cat filename | root | Ver el contenido del archivo message_1.txt |
| - | root | Anote los permisos por defecto del archivo message_1.txt |
| --- | redes | Los siguientes comandos se ejcutan como el usuario redes |
| $ cd /tmp | redes | Cambie el path al directorio tmp |
| $ cat filename | root | Intente ver el contenido del archivo message_1.txt |
| --- | root | Los siguientes comandos se ejcutan como el usuario root |
| # chmod o-r secrets.txt | root | Eliminar los permisos de lectura (r=read,w=write,x=execute) de los otros (u=user,g=group,o=others) |
| chmod 640 secrets.txt | root | Dar permisos de lectura y escritura al dueño(7=4(r)+2(w)+0(x)), permisos de lectura al grupo (4=4(r)+0(w)+0(x) |
| # adduser redes | root | Cree un usuario de nombre redes |
| # man adduser | root | Consulte la ayuda del comando adduser |
| # groups redes | root | Obtener los grupos a los que pertenece el usuario redes |
| # gpasswd -a redes root | usuario root | Adicione el usuario redes al grupo root |
| --- | redes | Los siguientes comandos se ejcutan como el usuario redes |
| $ groups | redes | Obtener los grupos a los que pertenece el usuario redes |
| $ cd /tmp | redes | Cambie el path al directorio tmp |
| $ cat filename | root | Observe el contenido del archivo message_1.txt |
| --- | root | Los siguientes comandos se ejcutan como el usuario root |
| # chmod +rw message.txt | root | Asigne permisos de lectura y escritura para todos los usuarios |
| # echo "holaa" >> mensaje.txt | root | Adicione la palabra 'holaa' al archivo mensaje.txt |
| # mv mensaje.txt mensaje_origen.txt | root | Cambie el nombre del archivo |
| # scp mensaje_origen.txt redes@192.168.104.21:/tmp/mensaje_destino.txt | root | Enviar el archivo mensaje.txt a una maquina remota, el archivo debe tener permisos de lectura para poder ser enviado |
| # ssh redes@192.168.104.21 | root | Acceda a la máquina remota |
| $ cat /tmp/mensaje_destino.txt | redes | Verifique el contenido del archivo |
| $ ls -l /tmp/mensaje_destino.txt | redes | Observe los permisos del archivo |

## Comandos alternos

| Comando   | ¿Quien lo ejecuta? | Descripción   |
|------|------|------|
| $ newgrp root | redes | Adicionar un grupo (root) sin hacer logout |
| # su redes | root | Acceder a una sesión como el usuario redes |
| # exit | root | Abandonar una sesión |