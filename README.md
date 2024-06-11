## Temario de Bash

### Introducción a Bash
- **¿Qué es Bash?**
  - Bash es un intérprete de comandos de Unix que provee una interfaz entre el usuario y el sistema operativo.
  - Historia y evolución de Bash.
  - Importancia en la administración de sistemas y desarrollo.

- **Entorno de trabajo**
  - Descripción del entorno de trabajo de Bash: terminal, shell, variables de entorno, etc.

### Comandos básicos de Bash
- **Comandos básicos**
  - Ejemplos adicionales: `ls -l`, `cd -`, `mkdir -p directorio/subdirectorio`, `rm -i archivo.txt`.

### Variables y expresiones
- **Variables en Bash**
  - Ejemplos adicionales: `nombre="Rafa"`, `echo "Hola, $nombre"`.
- **Expresiones aritméticas**
  - Ejemplos adicionales: `resultado=$((3 + 5))`, `resultado=$((10 / 2))`.

### Estructuras de control
- **Condicionales**
  - Ejemplos adicionales: `if [ "$edad" -ge 18 ] && [ "$edad" -lt 65 ]; then ... fi`.
- **Bucles**
  - Ejemplos adicionales: `for color in "${colores[@]}"; do ... done`.

### Funciones
- **Funciones en Bash**
  - Ejemplos adicionales: `function saludar { ... }`.

### Trabajo con archivos y directorios
- **Manipulación de archivos**
  - Ejemplos adicionales: `chmod +x script.sh`, `cat archivo1.txt archivo2.txt > archivo_concatenado.txt`.
- **Manipulación de directorios**
  - Ejemplos adicionales: `ln -s /ruta/a/archivo /ruta/a/enlace_simbolico`, `cd ..`.

### Expresiones regulares
- **Expresiones regulares en Bash**
  - Ejemplos adicionales: `grep "patrón" archivo.txt`, `if [[ "$correo" =~ ^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$ ]]; then ... fi`.

### Scripting avanzado
- **Depuración de scripts**
  - Ejemplos adicionales: `set -x`, `set -e`.
- **Control de procesos**
  - Ejemplos adicionales: `proceso &`, `kill -SIGTERM PID`.

### Ejercicios prácticos
- **Ejercicios prácticos avanzados**
  - Ejemplo adicional: Escribir un script que analice un archivo de registro y muestre estadísticas.
