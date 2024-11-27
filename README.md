# Practica06SUnix

# Instalar phpMyadmin desde codigo fuente

Primero haremos un apt update 

![image](https://github.com/user-attachments/assets/1249df67-bca9-4e34-89db-1957a9e23090)

Luego instalamos apache2

![image](https://github.com/user-attachments/assets/16718aee-165b-4a10-9677-1ec082fd75ad)

Despues de esto instalamos el servidor de base de datos MariaDB. MariaDB es un sistema de gestión de bases de datos derivado de MySQL y se utiliza para almacenar los datos de la aplicación web.

![image](https://github.com/user-attachments/assets/4bb81e4f-d9e7-4978-8d54-50db1f365335)

Ahotra configuramos la seguridad del servidor MariaDB. Este script interactivo ayuda a establecer una contraseña para el usuario root de MariaDB, eliminar usuarios anónimos, deshabilitar el inicio de sesión remoto para root, y eliminar la base de datos de prueba.

![image](https://github.com/user-attachments/assets/29cdd255-d5ac-4e46-9fea-976947bcab02)

![image](https://github.com/user-attachments/assets/65110f2c-d845-4e11-b145-2855dd288e42)


Iniciamos el cliente de línea de comandos de MariaDB para ejecutar comandos SQL en la base de datos.

![image](https://github.com/user-attachments/assets/baa05525-8b85-4724-b5cd-91901739e4d4)

Tenemos Apache instalado para servir tu contenido y MariaDB instalado para almacenar y gestionar tus datos. PHP es el componente de su configuración que procesará código para mostrar contenido dinámico al usuario final. Puede ejecutar scripts, conectarse a tus bases de datos MariaDB para obtener información, y entregar el contenido procesado a tu servidor web para que lo muestre.

Instalamos ahora  PHP y las bibliotecas necesarias para que PHP funcione con Apache y MariaDB. PHP es un lenguaje de programación del lado del servidor que permite la creación de contenido dinámico.

![image](https://github.com/user-attachments/assets/4737655d-bb72-4f3f-81dc-1bfced17b2d2)

si un usuario solicita un directorio al servidor, Apache buscará primero un fichero llamado index.html. Para indicar al servidor web que prefiera archivos PHP sobre otros, puede configurar Apache para que busque primero un archivo index.php.

Para ello, ejecute el siguiente comando para abrir el archivo dir.conf en un editor de texto con privilegios de root. 

![image](https://github.com/user-attachments/assets/e92d3a5c-9089-4d89-b15c-b1bd1d2dbe9f)


![image](https://github.com/user-attachments/assets/15976e58-99ce-48e4-a070-057c51a4cf46)

![image](https://github.com/user-attachments/assets/e8736462-bd81-41c2-9c61-2ab5c5979899)

Recargamos la configuracion de apache2 

![image](https://github.com/user-attachments/assets/ce995553-93aa-45c8-8aee-72e97e4eeef5)

Y verifficamos el estado actual de apache 

![image](https://github.com/user-attachments/assets/c5b87066-a387-4daa-b546-fede63a03e22)

# Instalación de phpMyAdmin y paquetes recomendados

Instala extensiones adicionales de PHP necesarias para el funcionamiento de phpMyAdmin

![image](https://github.com/user-attachments/assets/90a750b6-c040-4536-9300-ba50748b643f)

Descargamos el codigo fuente de phpMyadmin

![image](https://github.com/user-attachments/assets/303418dd-c9e5-43e9-b5b3-f503fea786a2)


Extraemos el archivo descargado con el comando tar xvf phpMyAdmin-4.9.7-all-languages.tar.gz y nos queda lo siguiente

![image](https://github.com/user-attachments/assets/edbd5cef-e95b-4413-8095-b890724f6a14)

Movemos el directorio phpMyAdmin-4.9.7-all-languages y todos sus subdirectorios al directorio /usr/share/, la ubicación donde phpMyAdmin espera encontrar sus ficheros de configuración por defecto. También renombrará el directorio en su lugar a sólo phpmyadmin.

![image](https://github.com/user-attachments/assets/b80f3ec0-4673-464e-8969-5e4287b25eb7)

Ahora configuramos lo siguiente:

Creamos un directorio temporal para phpMyAdmin. Este directorio es necesario para almacenar archivos temporales que phpMyAdmin pueda necesitar.
Cambiamos el propietario del directorio temporal a www-data, el usuario con el que corre Apache. Esto garantiza que phpMyAdmin pueda acceder y manipular los archivos en el directorio.
Copiamos el archivo de configuración de ejemplo de phpMyAdmin a un archivo de configuración real, que luego se puede editar para personalizar la configuración.

![image](https://github.com/user-attachments/assets/40f69e04-e5db-4371-85ae-24b11959db8a)

Instalamos la herramienta pwgen, que se utiliza para generar contraseñas aleatorias.
Y generamos una cadena segura de 32 caracteres para ser utilizada como valor para blowfish_secret.

![image](https://github.com/user-attachments/assets/19052d8a-3d1e-4815-aa35-62162b77fa58)

Ahora abrimos el siguiente archivo 

![image](https://github.com/user-attachments/assets/4e0b0ab5-faa3-43f1-899d-0a3549678b7c)

y ponemos la cadena de 32 caracteres 

![image](https://github.com/user-attachments/assets/397b96dd-c199-4310-ad43-bc5a864f0273)

Descomentamos estas lineas y las cambiamos

![image](https://github.com/user-attachments/assets/2a9ba902-fdfb-4235-9e9d-9f6e6cc9d6aa)

![image](https://github.com/user-attachments/assets/813844f5-6761-41dc-8f3f-bbb483a18879)


Tambien descomentamos estas lineas 

![image](https://github.com/user-attachments/assets/00a44d60-f92f-4511-b70b-3b403aec0f28)

![image](https://github.com/user-attachments/assets/3dbbf842-92cb-4724-af45-bed0c7240f1a)

Para despues crear las tablas

Vamos hasta la parte inferior del archivo y añada la siguiente línea. Esto configurará phpMyAdmin para usar el directorio /var/lib/phpmyadmin/tmp que creó antes como directorio temporal. phpMyAdmin usará este directorio temporal como caché de plantillas, lo que permite una carga más rápida de las páginas:

![image](https://github.com/user-attachments/assets/591a298f-87ed-473a-b286-897c32530868)








