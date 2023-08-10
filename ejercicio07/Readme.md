Para este ejercicio necesitas docker-compose, si estas usando Docker Desktop ya lo tienes instalado, sino deberás instalarlo aparte.Crea un archivo llamado "docker-compose.yml" y pon dentro el contenido de este link: https://gitlab.com/-/snippets/2376003/raw/main/docker-compose.yml.
A continuación ejecuta este comando en una terminal: docker-compose up.
Espera unos minutos hasta que dejen de aparecer mensaje en la terminal. Luego navega localhost:3000 para verificar que la aplicación levantó correctamente.
Finalmente contesta:
¿Cuántos contenedores se están ejecutando? (pueden verlo en el archivo docker-compose.yml y también ejecutando docker ps)
¿Cuales son las imágenes en las que están basados los mencionados contenedores?
¿Puedes leer el docker-compose.yml y describir lo que hace cada una de sus lineas?
Dado que cada contenedor corre en forma aislada ¿Cómo es posible que esos contenedores se vean entre sí?


Escribe tus respuestas ejercicio07/README.md en tu repositorio github y entrega el link directo al archivo.

¿Cuántos contenedores se están ejecutando? (pueden verlo en el archivo docker-compose.yml y también ejecutando docker ps)
-2 (db y web)

¿Cuales son las imágenes en las que están basados los mencionados contenedores?
-postgres:14.4-alpine
-nicopaez/jobvacancy-ruby:1.3.0

¿Puedes leer el docker-compose.yml y describir lo que hace cada una de sus lineas?
#Version de ESTE docker compose
version: '2'

#Declara servicios (containers)
services:
  web:
  #Declara imagen en la que se base
    image: nicopaez/jobvacancy-ruby:1.3.0
    #Declara alias para conectar con el servicio de db (para que esten en la misma red)
    links:
      - db
    #Bindea puerto 3000 al puerto 3000 del host
    ports:
      - "3000:3000"
    #Declara variables de entorno (donde se publica la db, puerto donde corre, variable de entorno (production) )
    environment:
      PORT: "3000"
      RACK_ENV: "production"
      DATABASE_URL: "postgres://postgres:Passw0rd!@db:5432/postgres"
    #Declara servicios (containers) de los cuales depende
    depends_on:
      - db
  db:
    #Declara imagen base
    image: postgres:14.4-alpine
#Declara variables de entorno (pwd de postgres)
    environment:
      POSTGRES_PASSWORD: Passw0rd!


Dado que cada contenedor corre en forma aislada ¿Cómo es posible que esos contenedores se vean entre sí?
-Con la instruccion (link) se especifca que ambos servicios (containers) puedan "verse".
