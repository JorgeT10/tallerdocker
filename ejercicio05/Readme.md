Investigar que hacen y para que se usan los siguientes comandos dentro de un Dockerfile:

* HEALTHCHECK
* ONBUILD
* VOLUME

Escribir la respuesta en el repositorio personal en ejercicio05/README.md, entregar el link director al archivo.

| Command     | Definition    | Documentation | Example |
|-------------|---------------|---------------|---------|
| HEALTHCHECK | The HEALTHCHECK instruction tells Docker how to test a container to check that it is still working. This can detect cases such as a web server that is stuck in an infinite loop and unable to handle new connections, even though the server process is still running.      | https://docs.docker.com/engine/reference/builder/#healthcheck  | ```Dockerfile HEALTHCHECK --interval=5m --timeout=3s CMD curl -f http://localhost/ || exit 1 ``` |
| ONBUILD     | The ONBUILD instruction adds to the image a trigger instruction to be executed at a later time, when the image is used as the base for another build. The trigger will be executed in the context of the downstream build, as if it had been inserted immediately after the FROM instruction in the downstream Dockerfile.      | https://docs.docker.com/engine/reference/builder/#onbuild  |``ONBUILD ADD . /app/src ONBUILD RUN /usr/local/bin/python-build --dir /app/src`` |
| VOLUME      | The VOLUME instruction creates a mount point with the specified name and marks it as holding externally mounted volumes from native host or other containers. The value can be a JSON array, VOLUME ["/var/log/"], or a plain string with multiple arguments, such as VOLUME /var/log or VOLUME /var/log /var/db. For more information/examples and mounting instructions via the Docker client, refer to Share Directories via Volumes documentation.   | [https://docs.docker.com/engine/reference/builder/#healthcheck ](https://docs.docker.com/engine/reference/builder/#volume) |``FROM ubuntu RUN mkdir /myvol RUN echo "hello world" > /myvol/greeting VOLUME /myvol`` |
