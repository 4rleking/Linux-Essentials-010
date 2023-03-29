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
