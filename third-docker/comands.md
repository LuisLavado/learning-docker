Explicación de instrucciones especificadas en el archivo Dockerfile:

WORKDIR = ubicacion donde se creara la aplicacion
COPY = copiar archivo local al entorno docker
RUN = ejecutar un comando dentro del contenedor
COPY . . = copiamos los fuentes dentro del WORKDIR especificado
CMD = ejecutar comando sh

________________________________________________________________
Para crear la imagen y después hacer el build utilicé los siguientes comandos

docker build -t api_python:latest ./
docker run -it --rm -d -p 8085:5000 --name api api_python

Tuve un problema con el puerto que comunica el contenedor a la aplicación (el segundo puerto), a diferencia de la página web, que nginx utiliza el puerto 80, flask utiliza por defecto el puerto 5000, por lo que si se quiere utilizar los puertos 8085:80 flask arrojara un error, ya que con el puerto 8085 el local se comunica al contenedor (Funciona siempre y cuando no estes ocupando ya ese puerto) y despues el contenedor intenta comunicarse al puerto 80 lo cual no tendrá nada ya que Flask está en el 5000.
________________________________________________________________
Desde la ruta del Dockerfile corremos

docker build -t app_python .

luego arrancamos el contenedor como es flask corre en el puerto 5000 docker run -it --rm -d -p 8081:5000 --name web_app_python app_python

ya podremos ver la api en la ruta


Si no tienes Python ni Flask instalados en la terminal de linux ubuntu, puedes seguir esta guía:

Instalar python: https://phoenixnap.com/kb/how-to-install-python-3-ubuntu
Instalar Flask: https://vegastack.com/tutorials/how-to-install-flask-on-ubuntu-20-04/