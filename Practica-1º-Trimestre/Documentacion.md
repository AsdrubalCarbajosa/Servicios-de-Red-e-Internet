# Práctica 1º Trimestre #
## Instalación del servidor web apache. Usaremos dos dominios mediante el archivo hosts: centro.intranet y departamentos.centro.intranet. El primero servirá el contenido mediante wordpress y el segundo una aplicación en python ##
Lo primero para instalar apache es actualizar las listas de paquetes, locual podemos hacer con este comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/599a38a5-f4c5-445f-bb64-279f99c0d180)

Luego ejecutamos este comando para instalar apache:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/37ae062e-65ac-4c3a-8888-b2f6377e8fa6)

Ahora nos vamos al fichero hosts que se encuentra en la carpeta **/etc**:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/05c6d3a8-e78a-452c-8ebc-575d31cf6c54)

En el fichero hosts añadimos los dos dominios que vamos a usar en este proyecto.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/23089073-8cfc-456d-b0b8-8bd5b93739b5)

## Activar los módulos necesarios para ejecutar php y acceder a mysql ##
Lo primero una vez descargado apache es descargar el soporte PHP y MySQL

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e0ed3471-14f5-4a5f-816a-79de5213815d)

Ahora vamos a editar el archivo de configuración de php **dir.conf** que se encuentra en **/etc/apache2/mods-enabled**

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e97b02c3-d793-4e99-826e-bd0786f44550)

El archivo de configuración tiene que quedar así:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4b4aac81-7069-4a3c-91c3-8624e0455a82)

Ahora reiniciamos apache con este comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/10f23540-d5a0-4c2b-ab1a-61b054af9afb)

Tras todo esto, vamos a instalar el servidor MySQL. Usaremos este comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f7d62172-e048-483c-bc49-867509f37eea)

Vamos a acceder a la línea de comandos de MySQL. La contraseña por defecto es **root**:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/b316274b-2bc7-4d7a-b33e-83d6220d0276)

Como es obvio, root no es una contraseña muy segura, por lo cual vamos a cambiarla.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4096946f-5bec-489d-a71d-a81ca5e634c2)
![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/b936c6cb-53cf-4be0-93ff-2cc26d8fb6c5)

Tras habernos salido, volvemos a acceder a MySQL con el comando de antes y la nueva contraseña:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/9f769698-a014-4216-babb-018257e212df)

## Instala y configura wordpress ##
Lo primero será descargar Wordpress desde su página oficial, lo cual podemos hacer directamente desde el siguiente comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/ccffa949-6451-4bb4-810a-f4215579df7c)

Antes de seguir, vamos a crear la base de datos que usaremos para Wordpress. Lo primero será meternos en MySQL. Acto seguido, creamos la base de datos, un nuevo usuario y le damos permisos al nuevo usuario sobre la base de datos que acabamos de crear, como se refleja en esta imagen:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/1c914a36-73f4-4398-a42d-d1b5b74c8fd9)

Ahora descomprimimos el paquete de Wordpress que descargamos anteriormente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4872ac75-fdae-48b0-966c-4e1b838945c3)

Y acto seguido lo movemos a la carpeta donde se alojan las páginas web en apache:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/ba53a65f-95d0-4fbd-a288-be0bb6d03b19)

Ahora le otorgamos permisos de escritura a la carpeta de contenidos de Wordpress para evitar errores relacionados con permisos:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e53dea8b-ecb3-4fd6-9fea-fcedb87c9546)



