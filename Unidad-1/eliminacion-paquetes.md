<h3>Eliminación de paquetes</h3>
  <p>Los mismos comandos utilizados para instalar paquetes se utilizan para eliminarlos. Todos los comandos aceptan la palabra clave "remove" para desinstalar un paquete instalado: "apt-get remove package_name" o "apt remove package_name" para paquetes DEB y "yum remove package_name" o "dnf remove package_name" para paquetes RPM. El comando "sudo" también es necesario para realizar la eliminación. Por ejemplo, para eliminar el paquete "figlet" instalado previamente en una distribución basada en DEB:</p>
  
```
$sudo apt-get remove figlet
  Reading package lists... Done
  Building dependency tree
  Reading state information... Done
  The following packages will be REMOVED:
    figlet
  0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.
  After this operation, 741 kB disk space will be freed.
  Do you want to continue? [Y/n] Y
```
  
  <p>Después de confirmar la operación, el paquete se borra del sistema:</p>
  
```
(Reading database ... 115775 files and directories currently installed.)
  Removing figlet (2.2.5-2) ...
  Processing triggers for man-db (2.7.6.1-2) ...
```
  
  <p>Un procedimiento similar se realiza en un sistema basado en rpm, por ejemplo, para eliminar el paquete "cowsay" previamente instalado de una distribución basada en RPM:</p>
  
```
$sudo yum remove cowsay
  Dependencies resolved.
================================================================================================================================
  Package                     Arch                     Version                      repository                          Size
================================================================================================================================
  Removing:
  cowsay                      noarch                  3.04-10.fc28                    @fedora                           76 k
  
  Transaction Summary
================================================================================================================================
  Remove 1 Package
  
  Freed space: 76 k
  Is this ok [y/N]: y
```
  
  <p>Asimismo, se solicita una confirmación y se borra el paquete del sistema:</p>
  
  
