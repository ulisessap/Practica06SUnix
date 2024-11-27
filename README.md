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


