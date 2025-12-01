# Create Docker Image from a Dockerfile

## Dockerfile:
FROM nginx:latest

### Path: /usr/share/nginx/html
COPY /sitio /usr/share/nginx/html 

## Create Docker image
docker build -t website:latest .

## Create Docker Container
docker run -it --rm -d -p 8080:80 --name web website

## Add Volume para una imagen sin Referencia del volume en un Dockerfile
docker run -it --rm -d -p 8080:80 -v ./sitio:/usr/share/nginx/html/sitio --name web website


docker build -t nginx .
docker run -it --rm -d -p 8080:80 -v ./sitio:/usr/share/nginx/html/sitio --name web nginx
docker run -it --rm -d -p 8080:80 -v D:/PROJECTS/learning-docker/second-docker/sitio:/usr/share/nginx/html/sitio --name web nginx
docker run -it --rm -d -p 8080:80 -v D:/PROJECTS/learning-docker/second-docker/sitio:/usr/share/nginx/html/sitio --name web sitioweb


Utilizar los recursos de la clase 6.

Crear la carpeta /assets dentro de la carpeta /sitio 
Descarga dos imágenes random y déjalas en /assets 
Ejecuta 
docker run -it --rm -d -p 8080:80 -v ./sitio:/usr/share/nginx/html/sitio --name web nginx 

Verificar en Docker Desktop el container "nginx" en la pestaña "Exec":

cd /usr/share/nginx/html/sitio
ls
assets linktree.html

cd assets
ls
batman.jpeg superman.jpg

rm batman.jpeg
ls
superman.jpg

Recuerda que la url cambió a: localhost:8080/sitio/linktree.html

En el archivo linktree.html utiliza: COPY (cuando el contenido es estático) VOLUMEN (cuando el contenido es dinámico)

Complejo.. pero ahí vamos.. gran curso y de gran utilidad.

En un entrevista técnica, la segunda pregunta fue si usaba Docker para crear contenedores, y por eso estoy aquí.