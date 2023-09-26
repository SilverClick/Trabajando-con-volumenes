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




