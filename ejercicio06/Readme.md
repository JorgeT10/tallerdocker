Crear un contenedor para la aplicación PasswordApi (del ejercicio 4) que esté basada en la imagen redhat-openjdk-18/openjdk18-openshift
disponible en la registry de Red Hat (https://catalog.redhat.com/software/containers/redhat-openjdk-18/openjdk18-openshift/58ada5701fbe981673cd6b10).


1. Escribe el dockerfile
2. Genera la imagen (docker build)
3. Publica la imagen en tu cuenta de Dockerhub


Pon el Dockerfile en tu repositorio Github en una carpeta ejercicio06. Agrega también en esa carpeta un archivo readme con el link a la imagen generada en dockerhub.
Entrega el link a la carpeta en el repositorio Github.



Steps:

0)Comment or uncomment the the FROM in docker file depending on your host platform (Apple silicon)
1) Run ``docker build -t passwordapi .`` .
2) Run ``docker run -p 8080:8080 --name pwdapi pwdapi`` to test
3) Browse in http://localhost:8080 . Should see the Swagger doc for the API.
4) Tag ``docker tag docker.io/library/pwdapi:latest giorgiopro10/ejercicio06:1.0.0``
5) Upload ``docker push giorgiopro10/ejercicio06:1.0.0``


Final image: https://hub.docker.com/r/giorgiopro10/ejercicio06
