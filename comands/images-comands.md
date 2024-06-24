

# contruction simple
docker build .

# Delete images
docker rmi -f <IMAGE ID>

# Construir una imagen a partir de un archivo Dockerfile 
docker build -t <nombre_de_imagen:tab> .
# Example with { "nombre_de_imagen": "website", "tab": "latest" }:
docker build -t website:latest .

# Construir una imagen desde un archivo Dockerfile sin la caché 
docker build -t <nombre_de_imagen> . -no-cache 

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


docker run: Comando para ejecutar un contenedor. -it: Indica que se desea abrir una terminal interactiva dentro del contenedor. --rm: Elimina el contenedor automáticamente después de detenerlo. -d: Ejecuta el contenedor en segundo plano (modo detached). -p 8080:80: Mapea el puerto 8080 del host al puerto 80 del contenedor. Esto significa que si accedes a localhost:8080 en tu máquina, se redirigirá al puerto 80 dentro del contenedor. --name web: Asigna el nombre "web" al contenedor. sitioweb: Es el nombre de la imagen que se utilizará para crear el contenedor.


Buscar en todas las imagenes por referencia
docker images --filter=reference='*:1.0'

Listar imagenes con su Id completo
docker images --no-trunc

Agregar una convencion a mi imagen (admin/website:latest)
docker image tag website:latest admin/website:latest

Eliminar una imagen por nombre y tag
docker rmi admin/website:latest
solo se eliminara la etiqueta, en caso otras imagenes tengan el mismo ID, no se borrarán





Listar imágenes locales 
docker images 

Eliminar una imagen 
docker rmi <nombre_imagen> 
Eliminar una imagen por IMAGE ID: se eliminarán todas las imagenes que comartan el ID
docker rmi <IMAGE ID> 
docker rmi -f <IMAGE ID> 


Eliminar todas las imágenes no utilizadas 
docker image prune 

Inicie sesión en Docker 
docker login -u <nombredeusuario> 

Publica una imagen en Docker Hub 
docker push <nombre_usuario>/<nombre_imagen> 

Buscar una imagen en Docker Hub 
docker search <nombre_imagen> 

Extraer una imagen de un Docker Hub 
docker pull <nombre_imagen>




