# Create Docker Image from a Dockerfile

## Dockerfile:
FROM nginx:latest

# Path: /usr/share/nginx/html
COPY /sitio /usr/share/nginx/html 

## Create Docker image
docker build -t website:latest .

## Create Docker Container
docker run -it --rm -d -p 8080:80 --name web website
docker run -it --rm -d -p 8080:80 --name web sitioweb
