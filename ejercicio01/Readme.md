1. Crea una página html que tenga tu nombre
2. Ejecuta una imagen nginx (https://hub.docker.com/_/nginx) para que sirva tu página. Para esto tendrás que utilizar el comando docker run y deberás investigar la documentación de la imagen nginx para descubrir cómo especificarle el contenido que el servidor debe servir.

Steps:
1) run ``docker pull nginx `` .
2) run ``docker run -p 8080:80 -v ${PWD}:/usr/share/nginx/html nginx`` (note you should be on the same directory ${PWD} to you local file).
3) browse http://localhost:8080/hello.html, an html with an ok message should be displayed.
