# Práctica 2º Trimestre #
## Instalación de programas ##

Lo primero es la instalación de apache, mysql, php, python y phpmyadmin

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/45b94736-4a81-4f21-a1bc-4d901efc05af)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8eed3a03-e0f7-4164-9d23-da197f4c6c1e)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/181e3b0f-4a49-482a-b538-c5665284370f)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8d66ab97-ba54-41f5-b69a-38b4a7995c83)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e56cbb60-907c-45e2-9341-ecb8b288060b)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/a31fe445-a2c4-438b-a44a-2c737c1f9fd5)

Añadimos la ruta de phpmyadmin al servidor de apache.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e373d815-4c44-454c-bd1a-f75431df7a79)

Ahora reiniciamos el servidor y accedemos a phpmyadmin mediante el navegador web.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/84ec8733-e30f-4133-aebb-9405ea72c28d)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/126c09ff-ce4e-4ff9-91c1-e24e028d0e2a)

## Creación y configuración de DNS ##

Descargamos bind9:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/dc175f51-5f8d-4ddd-ab7d-0e540ce73c47)

Una vez descargado, nos vamos a "/etc/bind" y creamos un nuevo fichero con la configuración para la zona.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/0ac1f538-939d-445d-a2d4-6123d0e17b41)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f5f17966-66e8-4270-a3cb-2f73de9dd498)

Ahora nos vamos al fichero "named.conf.local" y añadimos lo siguiente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/b4cbe48b-ca9b-4746-896c-5c1f8c5ede6d)

Ahora reiniciamos bind9 y comprobamos que funcione correctamente.

## Configuración de FTP con TLS ##

Descargamos vftpd

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f9603694-dec7-40ea-9369-d5656f8e604d)

Ahora creamos un usuario como prueba para la conexión

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/1cf27521-afd9-40d1-b09c-5b80c69e887a)

En el siguiente paso, crearemos un directorio donde guardar nuestras configuraciones de ftp y le cambiaremos el propietario a nuestro usuario administrador para asegurarnos de que nadie pueda acceder al mismo.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/78f65c14-ad64-403e-b8f9-917dfa1f6a60)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/f718cd66-501b-4dad-afdd-2ccd45b97792)

Ahora accedemos al siguiente archivo de configuración y nos aseguramos de que las siguientes líneas estén sin comentar:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/9a2b15ab-51be-4b62-b738-249118fbbee8)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/aed84c3e-a521-4e6c-a366-2471b7c371cb)

Por último, definimos el directorio que creamos anteriormente como el directorio predeterminado de FTP

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/7b89964d-95be-40c9-b920-323955d4431d)

A continuación vamos a configurar TLS para asegurar la conexión FTP. Ponemos el siguiente comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8c28564b-b61f-49e9-8996-b00a15d7deba)

Cuando lo ejecutemos nos pedirá información que será incorporada a nuestro certificado TLS.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/ef3296ec-63cf-4b01-a851-d44e35ab65f6)

Lo siguiente será configurar FTP para que use el certificado. Nos vamos al archivo de configuración de FTP y ponemos lo siguiente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/378c33f0-5827-413d-8c75-d884f013cbcf)

Ahora guardamos los cambios.

## Creación del dominio ##

Vamos a crear el dominio para que los usuarios puedan crear sus subdominios. Nos vamos a la carpeta /etc/bind y creamos un nuevo archivo. En este caso se llamará "domasd.local", que es el nombre que usaremos para el dominio en este caso.

En el fichero vamos a poner el nombre del dominio, el usuario root y el servidor DNS en el siguiente formato:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/5d898d97-c032-463d-9b18-789af053533f)

Guardamos el archivo y nos vamos al archivo de la misma carpeta llamado "named.conf.local"

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/0f2449cf-2408-4d29-afe0-f7bb393c9d79)

Aquí escribimos el nombre de nuestro dominio junto con el type "master" y la ruta a nuestro fichero de configuración.

Una vez hecho esto, ya tendremos creado nuestro dominio.

## Instalación y configuración de SSH y SFTP ##

Lo primero será instalar SSH.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/a7161e23-86d3-450e-b375-a855a76f28a4)

En el caso de que estemos usando un cortafuegos, deberemos permitir a SSH el acceso.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/608cb3e9-7aec-4a0d-b7f1-d66e74644386)

Ahora si nos conectamos desde el cliente por ssh al servidor nos permitirá el acceso:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/107682bb-4f4c-441d-a501-7c6581a8f750)

Si queremos conectarnos por sftp, solo deberemos escribir lo siguiente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/4c8d02b1-306c-4288-b2ae-d7dff30d960a)

Con esto tendríamos configurado tanto SSH como SFTP.

## Configuración de Postfix, Dovecot Imap y Pop3 ##

Instalamos Dovecot con el siguiente comando:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/68225048-aa56-4d68-8add-1b75b51c7ffd)

Durante la instalación nos aparecerá esta ventana. Seleccionamos la opción de internet.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/17555010-3f2d-4509-a41b-7c00ecaf4564)

Ahora elegimos cómo llamaremos a nuestro servidor de correo.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/2b945763-f1aa-4f46-ab2e-f145fccfa2e4)

Ahora nos vamos a nuestro fichero de configuración del dominio en bind y agregamos las siguientes líneas: 

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/69e421b8-bb24-4c83-a01d-b48946917c26)

Ahor reiniciamos bind9 y ya tendríamos creado nuestro servidor de correo.

## Creación de Scripts ##

Ahora vamos a crear un script para crear usuarios, su contraseña, el directorio de alojamiento web, el subdominio y el VirtualHost en Apache.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/7d564039-e79c-40c3-972c-1803b8d01e52)

Lo primero será definir las variables.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/9106e7d3-0c00-4b1d-9330-5e7547454381)

A continuación procedemos a la creación del usuario y su correspondiente directorio para el alojamiento web. Además, vamos a copiar dentro del directorio su correspondiente plantilla HTML.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/9947df72-4a7f-4592-9533-515c8445e198)

Ahora vamos a crear el subdominio para poder alojar la página web en nuestra carpeta de Bind9 que definimos anteriormente en las variables.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/fa4cb6b7-0dc8-4e9a-8b45-1341c38a761b)

Por último, creamos el VirtualHost en Apache mediante estos comandos. Incluiremos el nombre de la página web, el del administrador, la ruta del documento, y los permisos aplicados sobre el documento. Además, incluimos los certificados TLS para que el usuario cliente se pueda conectar de forma segura a través de FTP. Tras esto, activamos el sitio con "a2ensite" y reiniciamos los servicios.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/bd62a5b2-ed45-45ff-8583-260f54f4dd87)

Vamos a comprobar que funciona correctamente ejecutano el script:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/d746c3b6-c504-4612-8aec-25b48dd2d9bd)

Comprobamos que tanto en la carpeta de configuración de apache como en la de bind se ha añadido todo correctamente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/d69f649b-f606-4f64-8cfc-2bd149031c8e)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/b3561a4b-c5ca-4aa8-a210-0a3a1bd1912c)

Lo siguiente será la creación del script para la base de datos.

Primero solicitamos las credenciales de root para poder crear y modificar la base e datos e MySQL.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/58da484e-f699-4550-bae9-ac282588fbe4)

Ahora solicitamos el nombre de la nueva base de datos, el nombre del nuevo usuario, y su contraseña. Para las contraseñas usamos el comando -s para que los caracteres que introduzcamos no aparezcan en la pantalla del terminal, lo cual hace que el proceso sea mucho más seguro.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/af903f44-78a9-4512-9a8e-52e93a7e1f91)

Para finalizar procedemos a la creación de la base de datos con las credenciales que efinimos anteriormente.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/d6f1eb3c-e86e-4196-a7f0-afdfc0f66adf)

Ahora vamos a comprobar que funciona correctamente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/87beea8f-5fa7-48ce-a198-5f4cd45cb9dd)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/b911bee0-5a98-48a3-978d-3a2080de8a4e)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8467a7cd-9b2f-41c7-af46-c8c0fb501c8c)

Para finalizar los scripts, vamos a autorizar el uso  de aplicaciones python en las páginas web.
Antes que nada, vamos a crear un programa en python de ejemplo.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/2b43071c-7e0f-4da4-acc7-feeb00a3f258)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/55520344-cc58-417d-9cda-6c4c770bf987)

Ahora nos vamos al script que creamos anteriormente para la creación de los VirtualHost y añadimos lo siguiente:

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/cc4ecccc-7fe6-41ce-aa6f-ccb522240e76)

Con esto, cuando creemos un nuevo usuario se permitirá el uso de aplicaciones python.

