CMD: Ejecuta comandos **por default** dentro del container. Estos comandos, **NO** pueden ser sobreescritos.
Ejemplo:
Dentro de un dockefile
```CMD echo "This is a test." ```



ENTRYPOINT: Ejecuta comandos que son pasados por parametro (por ejemplo ```docker run <image> -d```) ```-d``` se pasa como argumento y a diferencia de ```CMD``` **SI** puede ser sobreescritos.
Ejemplo:
Dentro de un dockefile
```ENTRYPOINT ["top", "-b"] ```


Cabe destacar que CMD y ENTRYPOINT pueden ser combinados.
Por ejemplo:

``FROM alpine
ENTRYPOINT ["top"]
CMD ["-H"] ``
