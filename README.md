# Node.js y PostgreSQL, tarea Diplomado servicio Rest APIs - USIP

Servicios Rest Apis que pueden crear, recuperar, actualizar, eliminar y encontrar usuarios.

La siguiente tabla muestra una descripción general de los endpoint de las API Rest:

- GET     `api/usuarios`	               Obtiene todos los usuarios
- GET     `api/usuarios/:id`             Obtiene un usuario por su id
- POST    `api/usuarios`                 Adiciona o crea un usuario
- PUT     `api/usuarios/:id`             Actualiza un usuario por su id
- DELETE  `api/usuarios/:id`             Borra un usuario por su id
- GET     `api/usuarios/promedio-edad`   Devuelve el promedio de edad de los usuarios
- GET     `api/estado`                   Devuelve el estado de la aplicación

### Pruebas 
Para ejecutar el servicio Rest Api ejecute el siguiente comando: 
```
node server.js
```

Se uso Postman para realizar las pruebas de los servicios..

- Crea un nuevo usuario, usando `POST /usuarios` Api
![node-js-create](https://i.postimg.cc/x1Psdwt5/create.png)

Resultado:
```usip=# select * from usuarios;
 id |    username    |    password    |       email        | birthdate  |         createdAt       |         updatedAt
----+-------------+-------------------+-----------+------------------------------+-------------------------+----------------
  1 | grover         | MiPassword     | grover@correo.com  | 15/05/1999 | 2023-05-15 14:42:57.121 | 2023-05-15 14:42:57.121
  2 | americo        | MiPassword     | grover@correo.com  | 29/02/1980 | 2023-05-16 10:43:05.131 | 2023-05-16 10:43:05.131
 
```

- Obtiene todo los usuarios, usando `GET /usuarios` Api

![node-js-get-all](https://i.postimg.cc/vHCyzVsk/getAll.png)

- Obtiene un usuario por su id, usando `GET /usuarios/:id` Api

![node-js-get-id](https://i.postimg.cc/jSTgtxQC/getXId.png)

- Actualiza un usuario por su id, usando  `PUT /usuarios/:id` Api

![node-js-update](https://i.postimg.cc/28hcsbWP/update.png)

- Borrar a un usuario por su id, usando  `DELETE /usuarios/:id` Api

![node-js-delete](https://i.postimg.cc/zXGwjyjC/delete.png)

- Obtiene estado de la aplicación `/estado` Api

![node-js-delete](https://i.postimg.cc/s21s4dHf/estado.png)

- Obtiene el promedio de edad
![node-js-promedio](https://i.postimg.cc/6QjHNFhP/promedio.png)

## Base de datos
- Debe crearse una base de datos llamada usip
```
CREATE DATABASE usip;
```


## Project setup
```
npm install
```

