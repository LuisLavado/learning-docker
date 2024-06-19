# Create Docker Image from a Dockerfile

# contruction simple
docker build .

# Delete images
docker rmi -f <IMAGE ID>

# construction recomendated
docker build -t website:latest .

docker run -it --rm -d -p 8080:80 --name web website
docker run -it --rm -d -p 8080:80 --name web sitioweb

- -it: En forma interactiva para ver los logs

- --rm: elimina las versiones anteriores del contenedor

- -d: el contenedor se ejecuta en un segundo plano

- -p: mapea el puerto del contenedor con el puerto de la aplicación para exponerla

- --name: nombre del contenedor

- Finalmente agregar el nombre de la imagen


Con el comando docker ps también puedes incluir opciones adicionales para personalizar la salida:

-a (o --all): Muestra todos los contenedores, incluidos los detenidos.

--filter (o -f): Permite filtrar la salida según condiciones específicas, como la ID del contenedor, su nombre o su estado.

--format: Imprime la salida utilizando una plantilla de Go, lo que permite personalizar los campos que se muestran.

--size (o -s): Muestra información sobre el uso de disco por contenedor.

En resumen, docker ps es una herramienta útil para administrar y supervisar los contenedores en tu entorno Docker.

