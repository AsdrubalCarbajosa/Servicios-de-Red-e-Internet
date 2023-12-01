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


