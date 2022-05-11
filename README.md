# Entrega Laboratios y retos UND2

Aquí podra encontrar la entrega de los laboratarios de la unidad 2.

## Reto 2
En la carpeta de reto2 se encuentra todo lo relacionado y todo lo quese hizo al dockerizar el laboratirio 2, como tambiéne esta su respectivo reto
que consistía en darle una dirección DNS a la aplicación que montamos de WordPress utilizando docker.

## Reto 3
En la carpeta de reto3 se encuentra todo lo que se hizo con el laboratorio 3, al igual que en el laboratorio 2 se dcokerizo cada una de las capas de la aplicación y
se desplegaron tres instancias en EC2 de esta forma:

- Front End: Se abre los puertos de ssh, http, https
- Back End: Se abre los puertos de ssh y 5000 (Node.js), para las conexiones entrantes del frontEnd
- Base de datos (MongoDB): Se descarga MongoDB y se crea una base de datos llamada bookstore en la base de mongoDB, se abre el puerto 5000 para habilitar conexiones del BackEnd

1. Para el front end se nos entrego una aplicación en React la desplegamos con docker y la conectamos con la instancia de EC2 del back end para que así pueda tener comunicación con 
el servidor
2. Para el back end se nos entrego una aplicación en Node.js la desplegamos con docker y la conectamos con la base de datos en MongoDB, esta instancia manejaba el trafico
entrante en el frontEnd y realizaba las consultas correspondientes en el base de datos de mongoDB

## DNS y HTTPS
Para realizar ambos retos se necesitaba realizar la conexión a la aplicación con https, por eso a la solución a la que llegué fue dockerizar el certificado de mi dominio
que conseguí de forma gratuita en [Freenom](https://www.freenom.com/en/index.html?lang=en) y el certificado de https que coloque en el docker, es una imagen de una 
docker-compose de [letsencrypt](https://letsencrypt.org/), lo cual al volver a montar el docker me daba acceso a mi dominio por medio de https.

Los dominios para cada laboratorio son respectivamente:

Laboratorio 2
www.und2telematica.tk

Laboratorio 3
www.telematica-urrego-reto3.tk
