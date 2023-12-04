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

A continuación vamos a configurar Wordpress para que use la base de datos que hemos creado. Nos vamos al directorio de Wordpress, copiamos el archivo de ejemplo de configuración de Wordpress como un archivo de configuración normal y lo editamos:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/2ca5c920-5eff-4291-898c-0de87ea72ed6)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/cc2e9d6f-4430-4633-bdf9-12d280cb5aff)

Aquí ponemos el nombre de nuestra base de datos, nuestro usuario y nuestra contraseña.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/5eae21a9-df99-428d-a3c7-316e6daed75d)

Una vez hecho esto ponemos en nuestro navegador "localhost/nombredenuestracarpetadewordpress". Podemos empezar con la configuración de Wordpress.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f3d122ae-8878-4572-8df7-c4ed29027ad3)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e6864310-8098-436c-b45c-abee58d514b8)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4e22c1c6-3dff-456a-aba8-c9a510571e02)

## Activar el módulo wsgi para permitir la ejecución de aplicaciones Python

Podemos instalar el módulo wsgi desde el comando que se muestra a continuación:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/da62e849-ca01-4f50-b43e-53cc92940742)


Tras estos comandos ya tendremos instalado wsgi.

## Crea y despliega una pequeña aplicación python para comprobar que funciona correctamente

Lo primero es crear el directorio para alojar nuestra aplicación python, ademas de otro directorio para los archivos python y otro más para aplicaciones estáticas.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/a773d781-c6e7-423a-a732-8f53249ccdfa)

Ahora creamos el archivo python en la carpeta de los archivos Python.
NOTA: Es posible que tengas que cambiar los paermisos de la carpeta. Puedes usar el comando de arriba de la siguiente imagen:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/72394f7e-64d4-433f-989c-585e9bc41344)

Ahora editamos el archivo que acabamos de crear y añadimos lo siguiente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8059e040-188e-4df1-970e-f36f0d4cbd57)

Acto seguido creamos un nuevo virtualhost y ponemos la información necesaria.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e089a0d7-2c50-485b-9e63-6c531b408cf9)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f10e0787-a4bf-46ed-ad13-b240e539425a)

Si intentamos acceder ahora a la página que acabamos de crear nos debería de aparecer el mensaje que escribimos anteriormente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/09652ad7-1905-4b06-813a-c3fa58be54e6)

## Adicionalmente protegeremos el acceso a la aplicación python mediante autenticación

Lo primero será crear el fichero donde se almacenarán los usuarios y contraseñas de apache. Ponemos el siguiente comando poniendo al final del mismo el nobre de usuario que queramos. Acto seguido, introducimos una contraseña (en este caso, se usó el nombre de usuario usuario y la contraseña usuario).

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/652236a9-f9e7-463c-9bca-b17a7c34090b)

Si examinamos el archivo podremos ver el nombre del usuario y la contraseña cifrada.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/25823523-9db8-4879-a092-173383def48e)

Ahora nos vamos al directorio en el que se encuentra el archivo de configuración de nuestro servidor y lo abrimos.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/0b13ea70-0387-488e-9972-cdea9dbbcd14)

Una vez dentro, añadimos en la parte inferior la ruta donde se encuentra el contenido de nuestra aplicación python y le ponemos las siguientes directrices para que el acceso a esta requiera un nombre de usuario y contraseña válidos.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/ecd5e6ba-0788-4832-8466-e7615bdd4843)

Cuando hayamos terminado, reiniciamos apache.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/0074aff3-a890-491e-b324-cd7059406f80)

Si nos vamos ahora a la dirección web donde se encuentra alojada la aplicación apache podremos ver que se requiere un usuario y una contraseña.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e0051d88-5cde-48be-b49b-ee638eb4c182)

En caso de introducir las credenciales correctas nos aparecerá el contenido.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4d1cd0b9-1188-4fbc-bd56-34f4524fa70d)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/350ecd64-b1c7-41c2-af9f-fb6ceaa5e585)

Pero en caso de no teclear las credenciales correctas nos saltará un mensaje de error.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/2a4c1cc5-0144-451a-a734-7a94512d7fc3)

## Instala y configura awstat

Para empezar instalaremos awstat.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/c763cad7-7401-4dc8-b92b-92b44a9a68f2)

Ahora creamos un archivo de configuración en el directorio de configuraciones de apache.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/21357c35-49f7-4ad5-a293-ad95087222c0)

En el introducimos las directrices necesarias para la configuración de awstat.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f6c9c86b-6b79-46db-8242-463a7f73a8da)

Ahora activamos el módulo CGI, awstat y reiniciamos el servidor.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/57ff5b03-af1b-4e10-b2f5-f3d64e7489a1)

Accedemos al directorio de awstats en /etc/awstats y copiamos el archivo de configuración con el siguiente formato:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/68f7919e-ccf4-483b-8f07-cf9b1441cb94)

Es decir, añadiendo el nombre del dominio del que queremos ver las estadísticas.
Ahora editamos el archivo cambiando el nombre del archivo de datos y el nombre del dominio:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e112aedc-c05d-43b8-a44c-ac6653f7d62a)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/883a9652-5d88-41f2-8ef9-297b6254d440)

Ahora generamos el archivo con las estadísticas del dominio.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/08452165-6f5d-4b92-9504-91711b74bbca)

Una vez generado el archivo nos vamos al navegador y ponemos la dirección http://departamentos.centro.intranet/awstats/awstats.pl?config=departamentos.centro.intranet, cambiando el nombre del dominio por el que corresponda. Aquí podremos ver las estadísticas de nuestro dominio.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4070951d-4924-40f6-a00e-fce2c6b363af)

## Instala un segundo servidor de tu elección (nginx, lightpd) bajo el dominio "servidor2.centro.intranet". Debes configurarlo para que sirva en el puerto 8080 y haz los cambios necesarios para ejecutar php. Instala phpmyadmin.

Como siempre, lo primero es instalar el programa en cuestión, en este caso nginx.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4d86fce3-e195-4c5b-8719-ca1922fc8b3c)

Ahora creamos una carpeta para almacenar los archivos del nuevo dominio.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/a683a577-14de-44c1-b6bb-67d8d90757e0)

Ahora vamos a crear un archivo html simple para poder visualizar en la página web.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/2466bc4c-ee89-4691-b96d-9520aea9a6a3)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/61cfd42d-df5c-4584-b01f-a212bc579f90)

Acto seguido nos vamos al directorio en el que se alojan los sitios web de nginx y creamos uno nuevo con lo siguiente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/b50e1b2c-197f-4850-ba79-be1c07b83c46)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/404a4449-fe58-4a5d-b9f6-f4dee171d445)

Ahora si lo buscamos en el navegador en el puerto 8080 nos aparecerá el sitio.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/019652be-4819-46bf-b150-8d1a5452c8d6)

Ahora vamos a instalar phpmyadmin en nginx. ponemos el siguiente comando.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/ebd11b1b-511b-43f0-8e81-5c3028b1c1b2)

Cuando nos salga esta ventana le damos al tabulador en el teclado para no seleccionar ninguna de las opciones, debido a que no estamos usando ni apache ni lighttpd.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4b3f3e71-a4d4-4c15-8801-5fa12ea5ba97)

Aquí seleccionamos Sí.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/19ade871-472d-4c27-9cf2-f0d06faf3089)

Aquí creamos una contraseña para la base de datos.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/59a167c2-eccc-430e-86f0-92576116ed58)

Para que phpmyadmin funcione con nginx deberemos crear un enlace simbólico en el dominio en el que necesitamos la base de datos, lo cual crearemos con el siguiente comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/fe88fbb1-d3a8-4676-8a46-fa24f2ecd0b8)

