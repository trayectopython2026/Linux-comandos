# ¿Quién soy?
whoami

# ¿Dónde estoy?
pwd

# ¿Qué hay acá?
ls

ls                  # Listar archivos
ls -l               # Listar con detalles
ls -a               # Incluir ocultos
ls -alh             # Todo + tamaños legibles

# Creamos nuestro espacio de trabajo
mkdir curso_linux


# Entramos
cd curso_linux

# Comprobamos
pwd

# Miramos qué pasó
ls


# Creamos archivos

touch notas.txt

# Copiamos un archivo
cp notas.txt notas_backup.txt

# Renombramos
mv notas.txt apuntes.txt


# Información de nuestra PC
uname -a
free -h
df -h

# Vemos lo que estuvimos haciendo
history


# creacion de archivos
touch archivo.txt          # Crear archivo vacío
echo "texto" > archivo.txt     # Crear con contenido
echo "más" >> archivo.txt      # Agregar contenido

# mirar 
cat archivo.txt           # Ver todo
cat -n archivo.txt        # Con números de línea
head archivo.txt          # Primeras 10 líneas
head -n 5 archivo.txt     # Primeras 5 líneas
tail archivo.txt          # Últimas 10 líneas
tail -n 20 archivo.txt    # Últimas 20 líneas
wc -l archivo.txt         # Contar líneas

# eliminar

rm archivo.txt                  * Eliminar archivo
rm -r directorio/               * Eliminar directorio
rm -rf directorio/              * Forzar (¡CUIDADO!)
rmdir directorio_vacio/         * Solo directorios vacíos

# Usuario actual
whoami

# Info completa del usuario
id usuario

# Ver grupos del usuario
groups
groups usuario


# Crear usuario con home y shell
sudo useradd -m -s /bin/bash devops
# -m = crear directorio home
# -s = shell por defecto

# Eliminar usuario y su home
sudo userdel -r frontend

sudo groupadd grupo                 # Crear grupo
sudo groupdel grupo                 # Eliminar grupo

# Agregar usuario a grupo
sudo usermod -aG developers devops

 # chmod - Modo octal 

 # rwxr-xr-x = 755
chmod 755 ./test.txt

# rw-r--r-- = 644
chmod 644 ./test.txt

# rwx------ = 700
chmod 700 ./test.txt

# Permisos comunes:
# 755 = Scripts ejecutables, directorios
# 644 = Archivos normales
# 600 = Archivos privados (llaves SSH)
# 700 = Directorios privados (.ssh)
# 777 = TODO el mundo puede TODO (¡EVITAR!)

# Recursivo
chmod -R 755 ./directorio/


