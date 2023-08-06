1. Descarga la imagen nicopaez/pingapp:3.0.0
2. Crear un repositorio en dockerhub
3. Sube la imagen descargada al repositorio creado
4. Crea una carpeta "ejercicio02" en tu repositorio y pon dentro de la misma un archivo README.md con el detalle de instrucciones que utilizaste para completar la tarea.
5. Asegurate que la imagen queda publicada como pública.
6. Incluye al final de las instrucciones la sentencia docker pull exacta para descargar tu imagen.

Pista: utilizar comandos tag, login y push


Steps:
1) Pull ``docker pull nicopaez/pingapp:3.0.0 `` .

2) Create a repository on Docker Hub following these steps:
    Go to the Docker Hub website (https://hub.docker.com/) and log in to your Docker account or create one if you don't have it.
    Click the "Create Repository" button at the top right corner.
    Enter a name for your repository, e.g., "ejercicio02".
    You can add a description and configure the repository's visibility (public or private).
    Click the "Create" button to create the repository.

3)Upload the downloaded image to the created repository:    ``docker tag nicopaez/pingapp:3.0.0 giorgiopro10/ejercicio02:3.0.0`` .

3.1) Login ``docker login`` .

3.2) Push ``docker push giorgiopro10/ejercicio02:3.0.0`` .

4) Test it running: ``docker pull giorgiopro10/ejercicio02:3.0.0 `` .

4.1) Public link https://hub.docker.com/r/giorgiopro10/ejercicio02
