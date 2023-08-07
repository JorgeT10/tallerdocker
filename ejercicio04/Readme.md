Adjunto hay un archivo .jar que tiene la aplicación PasswordApi.
Esa aplicación es una aplicación Java que se ejecuta con el comando: java -jar passwordapi.jar. Eso levanta una webapi en el puerto 8080 (ver captura de pantalla).
Lo que se pide es generar una imagen Docker que corra esa aplicación. Más concretamente lo que hay que hacer es:
1. Escribir un dockerfile
2. Generar la imagen a partir del dockerfile ejecutando un docker build
3. Publicar la imagen en Dockerhub

Resolver el ejercicio en un directorio "ejercicio04" del repositorio personal.
Mencionar en el readme el link a la imagen publicada en dockerhub
Entregar el link a la carpeta del repositorio github.



Steps:

1) Run ``docker build -t passwordapi .`` .
2) Run ``docker run -d -p 8080:8080 --name passwordapi passwordapi``
3) Browse in http://localhost:8080 . Should see the Swagger doc for the API.
