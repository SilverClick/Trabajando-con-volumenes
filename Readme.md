# Tarea trabajando con volumenes 



1. **Descargar la imagen 'httpd' y comprobar que está en tu equipo**:
- Utilizamos el comando docker pull httpd para descargar la imagen de Docker llamada 'httpd'. Esta imagen contiene un servidor web Apache HTTPD.
Puedes verificar que la imagen se haya descargado correctamente utilizando el comando "docker images".

   ```bash
   docker pull httpd
   ```

2. **Crear un contenedor con el nombre 'dam_web1'**:

- Utiliza el siguiente comando para crear un contenedor con el nombre 'dam_web1':


   ```bash
   docker run -di --name dam_web1 httpd
   ```
- Esto creará un contenedor a partir de la imagen 'httpd' que acabas de descargar.

3. **Para acceder desde el navegador de tu equipo**:

- Si quieres poder acceder al servidor Apache desde tu navegador, debes mapear el puerto del contenedor al puerto de tu máquina. Puedes hacerlo al crear el contenedor con la opción `-p`, por ejemplo:

   ```bash
   docker run -di --name dam_web1 -p 8000:80 httpd
   ```

4. **Utilizar bind mount para montar el directorio 'htdocs' del Apache2**:

- Puedes montar un directorio de tu elección en tu sistema host con el directorio 'htdocs' del contenedor usando el siguiente comando:

   ```bash
   docker run -di --name dam_web1 -v "$PWD"/htdocs:/usr/local/apache2/htdocs/ httpd
   ```




