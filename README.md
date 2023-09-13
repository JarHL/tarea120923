# tarea120923
# Documentación de la tarea Permisos Ficheros

Este documento proporciona una descripción y los pasos necesarios para realizar cuatro tareas específicas en un sistema Linux. Cada tarea se ha numerado y se detallan a continuación.

## Tarea 1: Crear un Enlace Simbólico a Comando `cat`

**Descripción:** En esta tarea, se creará un enlace simbólico al comando `cat` y se ubicará en un directorio específico.

**Pasos:**
1. Abra una terminal de comandos en su sistema Linux.
2. Ejecute el siguiente comando para crear un enlace simbólico al comando `cat`:

   ```shell
   ln -s $(which cat) /home/kali/Documentos/tarea120923
   ```

## Tarea 2: Comprimir Archivos en un Archivo Tar.gz

**Descripción:** En esta tarea, se comprimirán varios archivos en un archivo `tar.gz`.

**Pasos:**
1. Asegúrese de que los archivos que desea comprimir, en este caso, `Aldo.txt`, `DPX.txt`, `Jared.txt`, `JaviV.txt`, `ONN.txt` y `ficheroAComprimir`, se encuentren en el mismo directorio, par ello en este caso se movieron a la carpeta ficheroAComprimir.
2. Abra una terminal de comandos en su sistema Linux.
3. Ejecute los siguientes comandos para comprimir los archivos:

   ```shell
   mv Aldo.txt DPX.txt Jared.txt JaviV.txt ONN.txt ficheroAComprimir
   tar -cvf ficheros.tar Aldo.txt Jared.txt JaviV.txt ONN.txt DPX.txt
   gzip ficheros.tar
   ```

## Tarea 3: Crear un Archivo Ejecutable para el Comando `ping`

**Descripción:** En esta tarea, se creará un archivo ejecutable que ejecutará el comando `ping 8.8.8.8` con permisos especiales.

**Pasos:**
1. Abra una terminal de comandos en su sistema Linux.
2. Cree un archivo llamado `ping8.8.sh` y ábralo en un editor de texto:

   ```shell
   nano ping8.8.sh
   ```

3. Dentro del archivo `ping8.8.sh`, agregue el siguiente contenido:

   ```shell
   ping 8.8.8.8
   ```

4. Guarde y cierre el archivo.
5. Ejecute los siguientes comandos para otorgar permisos especiales y de ejecución al archivo:

   ```shell
   chmod +s ping8.8.sh
   chmod +x ping8.8.sh
   ```

## Tarea 4: Crear un Directorio con Permiso Setgid

**Descripción:** En esta tarea, se creará un directorio con permisos Setgid.

**Pasos:**
1. Abra una terminal de comandos en su sistema Linux.
2. Ejecute los siguientes comandos para crear un directorio llamado `ficheroS` y establecer permisos Setgid en él:

   ```shell
   mkdir ficheroS
   chmod g+s ficheroS
   ```

Con estos pasos, ha completado las cuatro tareas especificadas. Cada tarea se detalla con sus pasos correspondientes para poder ejecutar las acciones necesarias en un sistema Linux.
### Referencias:
Gustavo, B. (2019, agosto 17). Cómo crear enlaces simbólicos en Linux. Tutoriales Hostinger. https://www.hostinger.mx/tutoriales/crear-enlace-simbolico-linux


