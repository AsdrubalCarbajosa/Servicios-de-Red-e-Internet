# Práctica 2º Trimestre #
## Instalación de programas ##

Lo primero es la instalación de apache, mysql, php y phpmyadmin
![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/45b94736-4a81-4f21-a1bc-4d901efc05af)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8eed3a03-e0f7-4164-9d23-da197f4c6c1e)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/181e3b0f-4a49-482a-b538-c5665284370f)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/8d66ab97-ba54-41f5-b69a-38b4a7995c83)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/a31fe445-a2c4-438b-a44a-2c737c1f9fd5)

Añadimos la ruta de phpmyadmin al servidor de apache.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/e373d815-4c44-454c-bd1a-f75431df7a79)

Ahora reiniciamos el servidor y accedemos a phpmyadmin mediante el navegador web.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/84ec8733-e30f-4133-aebb-9405ea72c28d)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/126c09ff-ce4e-4ff9-91c1-e24e028d0e2a)

## Configuración de FTP ##

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

Ahora vamos a crear un script para crear usuarios, su contraseña y el directorio de alojamiento web.

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/7d564039-e79c-40c3-972c-1803b8d01e52)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/2e9cbd89-fd47-45d6-a139-58a173380c40)

![image](https://github.com/AsdrubalCarbajosa/Servicios-de-Red-e-Internet/assets/91255302/be5cb2ab-e5d9-4f49-9b99-9a0696bec6ad)
