# Born2beroot 

<a href="https://github.com/gemartin99/Born2beroot-Tutorial">
Tutorial del Born2beroot
</a>

# Comandos de evaluación
1˚ Comprobar que no haya ninguna interfaz grafica en uso.

Utilizaremos el comando ```ls /usr/bin/*session``` y nos debe aparecer el mismo resultado que en la captura. Si aparece algo diferente se esta utilizando una interfaz grafica.

<img width="352" alt="Screen Shot 2022-11-25 at 12 00 02 AM" src="https://user-images.githubusercontent.com/66915274/203872315-0e87428b-5c5a-475b-9d7c-350eafbe3bea.png">

2˚ Comprobar que el servicio UFW esta en uso.

```sudo ufw status```

<img width="326" alt="Screen Shot 2022-11-24 at 1 25 06 AM" src="https://user-images.githubusercontent.com/66915274/203668014-bd228793-3532-4494-8b01-d046e4930c10.png">

```sudo service ufw status```

<img width="720" alt="Screen Shot 2022-11-24 at 1 25 37 AM" src="https://user-images.githubusercontent.com/66915274/203668066-6a3420d4-ae72-4263-8474-2e4946e2367a.png">

3˚ Comprobar que el servicio SSH esta en uso.

```sudo service ssh status```

<img width="711" alt="Screen Shot 2022-11-24 at 1 26 43 AM" src="https://user-images.githubusercontent.com/66915274/203668165-e642c21f-a11e-48b1-bed5-83639445251e.png">

4˚ Comprobar que utilizas el sistema operativo Debian o Centos.

```uname -v``` o ```uname --kernel-version```

<img width="306" alt="Screen Shot 2022-11-24 at 1 37 17 AM" src="https://user-images.githubusercontent.com/66915274/203669122-0be5033c-c882-4a2e-bf22-6a680f998a56.png">

5˚ Comprobar que tu usuario este dentro de los grupos "sudo" y "user42".

```getent group sudo```

```getent group user42```

<img width="314" alt="Screen Shot 2022-11-24 at 3 26 30 AM" src="https://user-images.githubusercontent.com/66915274/203680444-5fb18ae1-724e-4f78-a77f-a0f5bcc04913.png">

6˚ Crear un nuevo usuario y mostrar que sigue la politica de contraseñas que hemos creado.

```sudo adduser name_user``` y introducimos una contraseña que siga la politica.

<img width="465" alt="Screen Shot 2022-11-24 at 3 29 45 AM" src="https://user-images.githubusercontent.com/66915274/203680847-b4555fd4-f847-4bce-b944-edf3e7720c99.png">

7˚ Creamos un nuevo grupo llamado "evaluating". 

```sudo addgroup evaluating```

<img width="363" alt="Screen Shot 2022-11-24 at 3 30 47 AM" src="https://user-images.githubusercontent.com/66915274/203680980-784b2b60-82f4-405a-9f07-ec4948e86868.png">

8˚ Añadimos el nuevo usuario al nuevo grupo.

```sudo adduser name_user evaluating```

<img width="411" alt="Screen Shot 2022-11-24 at 3 33 08 AM" src="https://user-images.githubusercontent.com/66915274/203681233-096b200a-2b99-4638-81f3-a3bff046c0db.png">

Para comprobar que se haya introducido correctamente.

<img width="356" alt="Screen Shot 2022-11-24 at 3 33 31 AM" src="https://user-images.githubusercontent.com/66915274/203681267-106e4d37-0ec4-4006-95a4-88dd7109c4b6.png">

9˚ Comprobar que el hostname de la maquina es correcto login42.

<img width="224" alt="Screen Shot 2022-11-24 at 3 37 27 AM" src="https://user-images.githubusercontent.com/66915274/203681701-4f9b9ff1-28b6-4d06-9489-f930eee4b6e5.png">


10˚ Modificar hostname para remplazar tu login por el del evaluador. En este caso lo reemplazare por student42.

```sudo nano /etc/hostname``` y remplazamos nuestro login por el nuevo.

<img width="445" alt="Screen Shot 2022-11-24 at 3 42 30 AM" src="https://user-images.githubusercontent.com/66915274/203682323-dfd14846-9c98-48d0-9c83-56739de3220b.png">

<img width="525" alt="Screen Shot 2022-11-24 at 3 43 47 AM" src="https://user-images.githubusercontent.com/66915274/203682470-598a9dbf-ef28-4ef5-86cf-8caeef083ec3.png">

```sudo nano /etc/hosts``` y remplazamos nuestro login por el nuevo.

<img width="418" alt="Screen Shot 2022-11-24 at 3 44 08 AM" src="https://user-images.githubusercontent.com/66915274/203682512-5dd1452d-a704-466b-b9e1-89aa472fada6.png">

<img width="512" alt="Screen Shot 2022-11-24 at 3 44 35 AM" src="https://user-images.githubusercontent.com/66915274/203682562-36741000-6203-4a98-9de7-53afb24d6ea2.png">

Reiniciamos la maquina.

<img width="358" alt="Screen Shot 2022-11-24 at 3 44 58 AM" src="https://user-images.githubusercontent.com/66915274/203682614-60b10a36-c5d9-478b-a119-73e32a87b7fb.png">

Una vez nos hemos logueado de nuevo podemos ver como el hostname se ha cambiado correctamente.

<img width="263" alt="Screen Shot 2022-11-24 at 3 46 30 AM" src="https://user-images.githubusercontent.com/66915274/203682819-bd35ff17-3810-4644-9c44-93957e41d181.png">

11˚ Comprobar que todas las particiones son como indica el subject.

```lsblk```

<img width="495" alt="Screen Shot 2022-11-24 at 3 52 17 AM" src="https://user-images.githubusercontent.com/66915274/203683496-b49a7ada-2a0c-4f87-a013-e307370b3900.png">

12˚ Comprobar que sudo esta instalado.

```which sudo```

<img width="275" alt="Screen Shot 2022-11-24 at 4 00 42 AM" src="https://user-images.githubusercontent.com/66915274/203684520-1340d8dc-1b13-4828-9056-2631e659ddcf.png">

ó

```dpkg -s sudo```

<img width="789" alt="Screen Shot 2022-11-24 at 4 02 13 AM" src="https://user-images.githubusercontent.com/66915274/203684698-d66c3c5b-2d6b-43c5-8f63-1a3cddaf7b4d.png">

13˚ Introducimos el nuevo usuario dentro del grupo sudo.

```sudo adduser name_user sudo```

<img width="468" alt="Screen Shot 2022-11-24 at 5 02 24 AM" src="https://user-images.githubusercontent.com/66915274/203691378-2f2f5309-e650-486e-9cd6-cae4dec2ffa6.png">

Comprobamos que esta dentro del grupo.

 <img width="415" alt="Screen Shot 2022-11-24 at 5 02 39 AM" src="https://user-images.githubusercontent.com/66915274/203691402-6b84f333-10f7-4908-8255-652613afeede.png">

14˚ Muestra la aplicación de las reglas impuestas para sudo por el subject.

<img width="503" alt="Screen Shot 2022-11-24 at 5 12 02 AM" src="https://user-images.githubusercontent.com/66915274/203692615-bc1ec51c-ae5f-444f-9577-39b01112c969.png">

<img width="762" alt="Screen Shot 2022-11-24 at 5 12 17 AM" src="https://user-images.githubusercontent.com/66915274/203692638-e6de6cba-ad42-48b9-ac84-21e2b8c50563.png">

15˚ Muestra que la ruta /var/log/sudo/ existe y contiene almenos un fichero, en este se debería ver un historial de los comandos utilizados con sudo.

<img width="295" alt="Screen Shot 2022-11-24 at 5 17 54 AM" src="https://user-images.githubusercontent.com/66915274/203693244-39cb5903-7934-4f8a-8c39-f4ad94d305fb.png">

<img width="643" alt="Screen Shot 2022-11-24 at 5 19 07 AM" src="https://user-images.githubusercontent.com/66915274/203693358-b8a2832e-a80d-4304-b3be-43680ab9ba6d.png">

Ejecuta un comando con sudo y comprueba que se actualiza el fichero.

<img width="439" alt="Screen Shot 2022-11-24 at 5 23 08 AM" src="https://user-images.githubusercontent.com/66915274/203693791-21697c05-5087-4494-92ed-56ef9680f9fc.png">

<img width="661" alt="Screen Shot 2022-11-24 at 5 23 21 AM" src="https://user-images.githubusercontent.com/66915274/203693816-be7f7b83-d492-4d01-89cf-abff01d07d96.png">

16˚ Comprueba que el programa UFW esta instalado en la maquina virtual y comprueba que funciona correctamente.

```dpkg -s ufw```

<img width="730" alt="Screen Shot 2022-11-24 at 5 24 47 AM" src="https://user-images.githubusercontent.com/66915274/203693974-9e37e6d4-13a1-45b9-bb0d-03960a072694.png">

```sudo service ufw status```

<img width="704" alt="Screen Shot 2022-11-24 at 5 25 49 AM" src="https://user-images.githubusercontent.com/66915274/203694095-3bcf3a2e-04b8-4d63-a55c-b1e952e52dad.png">

17˚ Lista las reglas activas en UFW si no esta hecha la parte bonus solo debe aparecer la regla para el puerto 4242.

```sudo ufw status numbered```

<img width="500" alt="Screen Shot 2022-11-24 at 5 27 50 AM" src="https://user-images.githubusercontent.com/66915274/203694334-08b7791e-c7b6-4325-be60-7dc4e0257411.png">

18˚ Crea una nueva regla para el puerto 8080. Comprueba que se ha añadido a las reglas activas y acto seguido puedes borrarla.

```sudo ufw allow 8080``` para crearla

<img width="327" alt="Screen Shot 2022-11-24 at 5 31 35 AM" src="https://user-images.githubusercontent.com/66915274/203694718-09ae8097-e636-477d-bdc7-2d45ce892b72.png">

```sudo ufw status numbered```

<img width="473" alt="Screen Shot 2022-11-24 at 5 31 59 AM" src="https://user-images.githubusercontent.com/66915274/203694782-4f70c4a5-0de2-41ea-aba7-b1887e1fd517.png">

Para borrar la regla debemos utilizar el comando ```sudo ufw delete num_rule```

<img width="308" alt="Screen Shot 2022-11-24 at 5 33 15 AM" src="https://user-images.githubusercontent.com/66915274/203694914-82ae09cc-7e96-47db-b5ea-89e496f57db6.png">

Comprobamos que se ha eliminado y vemos el numero de la siguiente regla que hay que borrar.

<img width="467" alt="Screen Shot 2022-11-24 at 5 33 41 AM" src="https://user-images.githubusercontent.com/66915274/203694968-623554d2-f9c6-42db-aa34-c3c627b45f8e.png">

Borramos de nuevo la regla.

<img width="308" alt="Screen Shot 2022-11-24 at 5 34 03 AM" src="https://user-images.githubusercontent.com/66915274/203695003-deccc02f-ffc9-445a-a202-48b57cb66545.png">

Comprobamos que solo nos quedan las reglas requeridas en el subject.

<img width="461" alt="Screen Shot 2022-11-24 at 5 34 11 AM" src="https://user-images.githubusercontent.com/66915274/203695013-6b9ff40b-d23f-4a95-9694-f4e73e17f252.png">

19˚ Comprueba que el servicio ssh esta instalado en la maquina virtual, que funciona correctamente y que solo funciona por el puerto 4242.

```which ssh```

<img width="235" alt="Screen Shot 2022-11-24 at 5 37 25 AM" src="https://user-images.githubusercontent.com/66915274/203695373-c1cf2aca-15d5-4e7d-8c13-6e327824ae2c.png">

```sudo service ssh status```

<img width="616" alt="Screen Shot 2022-11-24 at 5 40 34 AM" src="https://user-images.githubusercontent.com/66915274/203695746-b8a3235d-6084-40c6-8cc0-83e78d0b497c.png">

20˚ Usa ssh para iniciar sesión con el usuario recién creado. Asegurate de que no puede usar ssh con el usuario root.

Intentamos conectarnos por ssh con el usuario root pero no tenemos permisos.

<img width="1377" alt="Screen Shot 2022-11-24 at 5 44 07 AM" src="https://user-images.githubusercontent.com/66915274/203696165-f1107b33-0c7e-4cce-8d04-56b845637ec8.png">

Nos conectamos por ssh con el nuevo usuario con el comando ```ssh newuser@localhost -p 4242```

<img width="1384" alt="Screen Shot 2022-11-24 at 5 48 06 AM" src="https://user-images.githubusercontent.com/66915274/203696612-f2c98ebf-be55-4830-b5ea-b0ac98de7c65.png">

21˚ Modifica el tiempo de ejecución del script de 10 minutos a 1.

Ejecutamos el siguiente comando para asi modificar el fichero crontab ```sudo crontab -u root -e```

<img width="455" alt="Screen Shot 2022-11-24 at 6 30 57 AM" src="https://user-images.githubusercontent.com/66915274/203701854-956c27de-367f-4b54-b21f-8a892d4891d4.png">

Modificamos el primer paramentro , en vez de 10 lo cambiamos a 1.

<img width="638" alt="Screen Shot 2022-11-24 at 6 31 44 AM" src="https://user-images.githubusercontent.com/66915274/203701944-393bd687-8b9c-4643-9d59-4789361e314d.png">

22˚ Finalmente haz que el script deje de ejecutarse cuando el servidor se haya iniciado, pero sin modificar el script.

```sudo /etc/init.d/cron stop```

<img width="483" alt="Screen Shot 2022-11-24 at 3 25 53 PM" src="https://user-images.githubusercontent.com/66915274/203807610-d87124f2-47ca-4546-8037-b904e8bcf5d1.png">

Si queremos que vuelva a ejecutarse:

```sudo /etc/init.d/cron start```

<img width="483" alt="Screen Shot 2022-11-24 at 3 27 38 PM" src="https://user-images.githubusercontent.com/66915274/203807970-8fc69a39-6d10-4e64-9be1-eb49c4bf95f8.png">
