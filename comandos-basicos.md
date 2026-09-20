# ¿Quién soy?
whoami

# ¿Dónde estoy?
pwd

# ¿Qué hay acá?
ls

- `ls` — Listar archivos
- `ls -l` — Listar con detalles
- `ls -a` — Incluir archivos ocultos
- `ls -alh` — Mostrar todo con tamaños legibles

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


## Creación de archivos

- `touch archivo.txt` — Crear archivo vacío
- `echo "texto" > archivo.txt` — Crear con contenido
- `echo "más" >> archivo.txt` — Agregar contenido

## Mirar

- `cat archivo.txt` — Ver todo
- `cat -n archivo.txt` — Ver con números de línea
- `head archivo.txt` — Ver las primeras 10 líneas
- `head -n 5 archivo.txt` — Ver las primeras 5 líneas
- `tail archivo.txt` — Ver las últimas 10 líneas
- `tail -n 20 archivo.txt` — Ver las últimas 20 líneas
- `wc -l archivo.txt` — Contar líneas

## Eliminar

- `rm archivo.txt` — Eliminar archivo
- `rm -r directorio/` — Eliminar directorio
- `rm -rf directorio/` — Forzar eliminación (**¡CUIDADO!**)
- `rmdir directorio_vacio/` — Eliminar solo directorios vacíos

# Usuario actual
whoami

# Info completa del usuario
id usuario

# Ver grupos del usuario
groups
groups usuario


# Crear usuario con home y shell
sudo useradd -m -s /bin/bash devops
### -m = crear directorio home
### -s = shell por defecto

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
### 755 = Scripts ejecutables, directorios
### 644 = Archivos normales
### 600 = Archivos privados (llaves SSH)
### 700 = Directorios privados (.ssh)
### 777 = TODO el mundo puede TODO (¡EVITAR!)

# Recursivo
chmod -R 755 ./directorio/


