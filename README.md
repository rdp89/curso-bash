### Temario para Curso de Bash

#### **Módulo 1: Introducción a Bash**
1. **Qué es Bash**
   - Historia y versiones.
   - Ventajas y usos comunes.
2. **Primeros pasos en la terminal**
   - Abrir la terminal.
   - Comandos básicos: `ls`, `pwd`, `cd`, `echo`.
   - Ejemplo:
     ```bash
     echo "Hola, Mundo"
     ```

#### **Módulo 2: Navegación y Gestión de Archivos**
1. **Comandos de navegación**
   - `cd`, `pwd`, `ls`, `tree`.
   - Ejemplo:
     ```bash
     cd /home/user
     pwd
     ls -l
     ```
2. **Manipulación de archivos y directorios**
   - Crear, copiar, mover, renombrar y eliminar archivos/directorios (`touch`, `cp`, `mv`, `rm`, `mkdir`, `rmdir`).
   - Ejemplo:
     ```bash
     touch archivo.txt
     mkdir carpeta
     mv archivo.txt carpeta/
     ```
3. **Permisos de archivos**
   - Comandos `chmod`, `chown`, `chgrp`.
   - Ejemplo:
     ```bash
     chmod 755 archivo.txt
     chown user:grupo archivo.txt
     ```

#### **Módulo 3: Trabajando con Texto**
1. **Comandos para manipulación de texto**
   - `cat`, `more`, `less`, `head`, `tail`.
   - Ejemplo:
     ```bash
     cat archivo.txt
     head -n 10 archivo.txt
     ```
2. **Buscar y filtrar texto**
   - `grep`, `sort`, `uniq`, `wc`.
   - Ejemplo:
     ```bash
     grep "palabra" archivo.txt
     sort archivo.txt | uniq
     wc -l archivo.txt
     ```

#### **Módulo 4: Redirección y Pipes**
1. **Redirección de entrada y salida**
   - `>`, `>>`, `<`, `<<`.
   - Ejemplo:
     ```bash
     echo "Texto" > archivo.txt
     cat archivo.txt >> archivo_copia.txt
     ```
2. **Uso de pipes (`|`)**
   - Conectar comandos.
   - Ejemplo:
     ```bash
     cat archivo.txt | grep "palabra"
     ```

#### **Módulo 5: Variables y Operaciones**
1. **Variables en Bash**
   - Definición y uso.
   - Ejemplo:
     ```bash
     nombre="Mundo"
     echo "Hola, $nombre"
     ```
2. **Operaciones aritméticas**
   - `expr`, `$(( ))`.
   - Ejemplo:
     ```bash
     resultado=$((5 + 3))
     echo $resultado
     ```

#### **Módulo 6: Estructuras de Control**
1. **Condicionales (`if`, `else`, `elif`)**
   - Sintaxis y ejemplos.
   - Ejemplo:
     ```bash
     if [ -f archivo.txt ]; then
       echo "El archivo existe"
     else
       echo "El archivo no existe"
     fi
     ```
2. **Bucles (`for`, `while`)**
   - Sintaxis y ejemplos.
   - Ejemplo:
     ```bash
     for i in {1..5}; do
       echo "Número $i"
     done
     ```

#### **Módulo 7: Funciones en Bash**
1. **Definición y uso de funciones**
   - Crear y llamar funciones.
   - Ejemplo:
     ```bash
     function saludo {
       echo "Hola, $1"
     }
     saludo Mundo
     ```

#### **Módulo 8: Scripts Avanzados**
1. **Parámetros y argumentos en scripts**
   - Uso de `$1`, `$2`, etc.
   - Ejemplo:
     ```bash
     #!/bin/bash
     echo "El primer argumento es $1"
     ```
2. **Depuración de scripts**
   - Uso de `set -x` y `set +x`.
   - Ejemplo:
     ```bash
     set -x
     ls
     set +x
     ```

#### **Módulo 9: Gestión de Procesos**
1. **Control de procesos**
   - `ps`, `top`, `kill`.
   - Ejemplo:
     ```bash
     ps aux | grep bash
     kill -9 PID
     ```

#### **Módulo 10: Automatización y Tareas Programadas**
1. **Uso de `cron` y `crontab`**
   - Programar tareas.
   - Ejemplo:
     ```bash
     # Editar crontab
     crontab -e
     # Añadir tarea: ejecutar script.sh cada día a las 2am
     0 2 * * * /ruta/a/script.sh
     ```

### Ejemplo de Proyecto Final
Desarrollar un script que realice una copia de seguridad de un directorio específico, comprimiéndolo y moviéndolo a otra ubicación con una estructura de nombres basada en la fecha y hora.

```bash
#!/bin/bash
# Script de copia de seguridad

# Directorios
ORIGEN="/ruta/al/directorio"
DESTINO="/ruta/de/backup"

# Nombre del archivo de backup con fecha y hora
FECHA=$(date +%Y%m%d_%H%M%S)
BACKUP="backup_$FECHA.tar.gz"

# Crear el archivo comprimido
tar -czf $DESTINO/$BACKUP $ORIGEN

# Mostrar mensaje de éxito
echo "Copia de seguridad completada: $DESTINO/$BACKUP"
