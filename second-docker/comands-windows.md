Las sentencias que se aplican en la clase es todo orientado a linux para el caso puntual Windows se deben hacer los siguientes cambios.

1. Modificar Dockerfile para que la ruta de copia de los archivos no se html sino sitio en el contenedor

#**********************************************

FROM nginx:latest

# Path del sitio

COPY /sitio /usr/share/nginx/html/sitio #**********************************************

2. Generar una nueva imagen con el cambio del Dockerfile

docker build -t nginx:1.0 .

3. Lanzar el nuevo contenedor basado en la nueva imagen, pero se debe orientar la ruta de archivos de "./sitio" (ruta ubuntu) a "disco:\ruta_de_la_carpeta_windows" (ruta en Windows) ejem: "D:\cursodocker\sitio"

docker run -it --rm -d -p 8080:80 -v D:\cursodocker\sitio:/usr/share/nginx/html/sitio --name web nginx:1.0
docker run -it --rm -d -p 8080:80 -v D:/PROJECTS/learning-docker/second-docker/sitio:/usr/share/nginx/html/sitio --name web nginx