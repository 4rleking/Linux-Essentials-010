# Instalación de paquetes
<p><a href=../README.md>Atrás</a</p>
  
  <p>Suponga que ha oído hablar de un comando llamado "figlet" que imprime texto agrandado en el terminal y desea probarlo; sin embargo, obtendrá el siguiente mensaje después de ejecutar el comando "figlet":</p>
  
  ```
  $figlet
  -bash: figlet: command not found
  ```

  <p>Esto significa que probablemente el paquete no esté instalado en su sistema. Si su distribución funciona con paquetes DEB, puede buscar en sus repositorios usando "apt-cache search package_name" o "apt search package_name". El comando "apt-cache" se usa para buscar paquetes y para listar información sobre paquetes disponibles. El siguiente comando busca cualquier ocurrencia del término "figlet" en los nombres y descripciones del paquete:</p>
  
  ```
  $apt-cache search figlet
  figlet - Make large character ASCII banners out of ordinary text
  ```
  
  <p>La búsqueda identificó un paquete llamado "figlet" que corresponde al comando que falta. La instalación y eliminación de un paquete requiere permisos especiales otorgados solo al administrador del sistema: el usuario llamado "root". En los sistemas de escritorio, los usuarios comunes pueden instalar o eliminar paquetes anteponiendo el comando "sudo" a los comandos de instalación y/o eliminación. Esto requerirá que escriba su contraseña para continuar. Para los paquetes DEB, la instalación se realiza con el comando "apt-get install package_name" o "apt install package_name":</p>

  ```
  $sudo apt-get install figlet
  Reading package lists... Done
  Building dependency tree
  Reading state information... Done
  The following NEW packages will be installed:
    figlet
  0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
  ```

  <p>En este punto el paquete se descargará e instalará en el sistema, así como las dependencias que eventualmente necesite el paquete:</p>
  
    ```
  Need to get 184 kB of archives.
  After this operation, 741 kB of aditional disk space will be used.
  Get:1 *http://archive.raspbian.org/raspbian stretch/main armhf figlet armhf 2.2.5-2 [184 kB]
  ```
