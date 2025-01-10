![Foto 1](1.png)
Creamos el archivo test.sh con un nano y añadimos el contenido para que muestre Hello World y lo guardamos con Ctrl+o y nos salimos con Ctrl+x


![Foto 2](2.png)

Despues le damos permisos para poder ejecutarlo

![Foto 3](3.png)

Lo ejecutamos y podemos ver que nos muestra el Hello Word

![Foto 4](4.png)

Revisamos los permisos y vemos que estan bien justo como los hemos puesto porque les hemos dado todos 

![Foto 7](7.png)

Creamos el fichero ncs dentro de home y le damos permisos (En la captura sale que pongo chmod 777 pero despues los vuelvo a cambiar a 644) y ponemos el script hello.sh

![Foto 5](5.png)

Creamos el usuario bob y cuando nos cambiamos de usuario y usamos el usuario bob, cuando intentamos ver a la carpeta /home/ncs la podemos ver pero si intentamos ejecutar el fichero de dentro el script hello.sh no podemos ejecutarlo porque bob no tiene permisos para ejecutarlos

![Foto 8](8.png)

Despues creamos el script bob.sh que al ejecutarlo nos muestra Hello this is Bob y lo podemos ejecutar sin problemas porque al crearlo con bob podemos ejecutarlo con bob porque va a tener permisos

![Foto 6](6.png)

Creamos el usuario smith y lo usamos y podemos ver el contenido de la carpeta /home/ncs pero no podemos ejecutar ninguno de los dos comandos porque smith no tiene permisos para ejecutarlos

![Foto 9](9.png)

Creo un grupo y añado a todos los usuarios y despues voy a cambiar al propietario del grupo de la carpeta y los archivos y va a ser el nuevo grupo con los usuarios y despues voy a poder ejecutar los dos archivos con los dos usuarios ya que ahora pertenecen al grupo del propietario y despues vamos a deshabilitar al usuario smith del grupo usando sudo usermod -L smith