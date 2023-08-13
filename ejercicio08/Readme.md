Utilizando docker compose generar una configuración para correr dos instancias de passwordapi (nicopaez/password-api) balanceadas por Nginx.
La aplicación tiene un endpoint /health que indica la ip/host de la instancia que atendió el pedido, se puede usar esto para verificar el correcto balanceo.
Poner la solución en un carpeta ejercicio08, incluyendo
la configuración de compose
el README.md con la forma correrlo y cualquier explicación que consideres relevante.

Steps

1) run ``docker-compose up --scale pwdapi=2``
2) Browse http://localhost:4000/health
