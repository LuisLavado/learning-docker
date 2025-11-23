Construir la imagen de Docker
Desde la terminal y en el directorio donde se encuentra tu Dockerfile, ejecuta el siguiente comando para construir tu imagen de Docker:

docker build -t nextjs-app .


Correr un contenedor Docker
Una vez que la imagen esté construida, puedes iniciar un contenedor utilizando esta imagen:

docker run -p 3000:3000 nextjs-app


Este comando ejecutará la aplicación y mapeará el puerto 3000 del contenedor al puerto 3000 de tu máquina local, permitiéndote acceder a la aplicación desde http://localhost:3000.

Consideraciones Finales
Asegúrate de mantener tu Dockerfile y dependencias actualizadas.
Utiliza volúmenes para el desarrollo local para que no tengas que reconstruir la imagen cada vez que hagas un cambio en el código.
Puedes optimizar tu imagen para producción minimizando las capas y archivos innecesarios.
Con estos pasos, puedes comenzar a desarrollar tu proyecto Next.js en un entorno Dockerizado.