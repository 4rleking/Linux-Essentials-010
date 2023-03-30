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
  Get:1 http://archive.raspbian.org/raspbian stretch/main armhf figlet armhf 2.2.5-2 [184 kB]
  Fetched 184 kB in 0s (213 kB/s)
  Selecting previously unselected package figlet.
  (Reading database ... 115701 files and directories currently installed.)
  Preparing to unpack .../figlet_2.2.5-2_armhf.deb ...
  Unpacking figlet (2.2.5-2) ...
  Setting up figlet (2.2.5-2) ...
  update-alternatives: using /usr/bin/figlet-figlet to provide /usr/bin/figlet (figlet) in auto mode
  Processing triggers for man-db (2.7.6.1-2) ...
  ```
  <p>Una vez finalizada la descarga, todos los archivos son copiados a las ubicaciones correspondiente, se realizará cualquier configuración adicional y el comando estará disponible:</p>
  
  <p>En distribuciones basadas en paquetes RPM, las búsquedas se realizan usando "yum search package_name" o "dnf search package_name". Supongamos que desea mostrar algún texto de una forma más irreverente, seguido de una vaca caricaturesca, pero no está seguro del paquete que puede realizar esa tarea:</p>
    
```
$yum search speaking cow
last metadata expiration check: 1:30:49 ago on Tue 23 Apr 2019 11:02:33 PM -03.
================ Name & Summary Matched: speaking, cow ========================
    cowsay.noarch : Configurable speaking/thinking cow
```
  <p>Después de encontrar un paquete adecuado en el repositorio, puede instalarse con "yum install package_name" o "dnf install package_name":</p>
  
```
$sudo yum install cowsay
 Last metadata expiration check: 2:41:02 on Tue 23 Apr 2019 11:02:33 PM -03.
 Dependencies resolved.
  
 Total download size: 46 k
 Installed size: 76 k
 Is this ok [y/N]: y
```
  <p>Una vez más, el paquete deseado y todas sus posibles dependencias serán descargados e instalados:</p>

```
Downloading Packages:
cowsay-3.04-10.fc28,noarch.rpm                                                                      490 kB/s | 46 kB    00:00
==============================================================================================================================
Total                                                                                                53 kB/s | 46 kB    00:00

  Running transaction check
  Transaction check succeeded.
  Running transaction test
  Transaction test succeeded.
  Running transaction
  Preparing         :                                                                                                   1/1
  Installing        : cowsay-3.04-10.fc28.noarch                                                                        1/1
  Running scriptlet : cowsay-3.04-10.fc28.noarch                                                                        1/1
  Verifying         : cowsay-3.04-10.fc28.noarch                                                                        1/1  
  
  Installed:
  cowsay-3.04-10.fc28.noarch
  
  Complete!
```
