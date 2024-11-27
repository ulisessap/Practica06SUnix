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


