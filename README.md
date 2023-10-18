# kidsing-backend

# Instalacion - npm init
Para poder utilizar el código necesitas las siguientes instalaciones:
For use the code need the next instalations:

npm i
or
npm i auth0 axios bcrypt body-parser cors dotenv express mysql


# Carpetas
-CONFIG
En la carpeta config está la información de la base de datos local (mirar los campos por si necesitan modificación).
Config is where you can see all the information about local database - see the information maybe you should do some changes -

-DUMP
En la carpeta dump está el archivo mysql, puedes encontrar la información para crear una nueva basededatos si lo necesitas.
The folder dump is where you can find the mysql file and all the information about the database. if u dont have it u can use to create one.

# Backend Code 
PROCEDIMIENTO 

Las instalaciones se usan para lo siguiente:

-auth0: paquete para usar un login de la propia compañía Auth0 que permite entrar con Google
-axios: paquete facilita el código
-bcrypt: se utiliza para poder usar la codificación que jsw de Auth0
-body-parser: para poder leer los datos que se envían del frontend al backend
-cors: paquete facilita el código
-dotenv: para guardar información personal/contraseñas/configuracion...
-express: para poder conectar el servidor y gestionarlo
-mysql: para poder conectar a la base de datos mysql

1º- Se crea una base de datos mysql para poder hacer la conexión
2º- Como la intención es modular el código para tener mejor organización hice un archivo donde se crea la conexión a la base de datos, de
esta forma se nos ahorramos utilizar este código que usaríamos muchas veces accesible por si necesitamos modificar el código.
3º- procedemos a crear la conexión con Auth0:
    -En la página web se crea un usuario y un servicio de login que proporciona el dominio, la contraseña y el ID. Ponemos esta información el archivo .env
    -Crearemos una ruta get para poder enviar esta información al frontend donde la recibirá para poder entrar al login
    -Junto a esta crearemos una ruta post para poder usar esta informacion del usuario
4º- Funcionando la conexión al servicio de Auth0 crearemos otra API para los jugadores, de esta forma podremos tener varios jugadores en la misma cuenta de usuario.
Esto se hará con la información del usuario registrado en la API del usuario, con esta información crearemos rutas para la creación de un jugador y mostrar todos los jugadores. Mientras hacía las API de usuarios y jugadores, me creaba una frontend muy básico para poder verificar la funcionalidad. Como tenemos claro el método y la tecnologías que usaríamos, utilice el React de la forma que usábamos en el proyecto

5º- Una vez solucionando los errores y comprobando la funcionalidad. Procedo a ayudar al frontend donde hay mucha más carga de trabajo

en el frontend procedere a hacer las páginas relacionadas con el backend, facilitando la implementación el código bakend con el frontend y arreglando y poniendo bonito las rutas de ver jugadores y crear jugadores que ya había hecho
También me dedicaré a unificar el código(frontend-data-backend) y crearé rutas para los componentes que estamos creando