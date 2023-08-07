Investigar que hacen y para que se usan los siguientes comandos dentro de un Dockerfile:

* HEALTHCHECK
* ONBUILD
* VOLUME

Escribir la respuesta en el repositorio personal en ejercicio05/README.md, entregar el link director al archivo.


All the below instruction can be used in a docker file, as an example a docker file is provided in the folder.

| Instruction     | Definition    | Documentation |
|-------------|---------------|---------------|
| HEALTH CHECK | The HEALTHCHECK instruction is used to provide if the container is healthy and this check can be parametrized by interval, retries, timeout, etc, also this instruction can disable the base image health check with    HEALTHCHECK NONE   | https://docs.docker.com/engine/reference/builder/#healthcheck  |
| ONBUILD     | The ONBUILD instruction is used to to run commands and that commands will be run when the image is use as a base image, this can be combine with other instrucctions such as run, HEALTHCHECK or VOLUME     | https://docs.docker.com/engine/reference/builder/#onbuild  |
| VOLUME      | The VOLUME instruction creates a Volume that is used for persist data within the container.   | [https://docs.docker.com/engine/reference/builder/#healthcheck ](https://docs.docker.com/engine/reference/builder/#volume), https://docs.docker.com/storage/volumes/ |
