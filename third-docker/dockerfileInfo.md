Dejaré por aquí algunos comando útiles para el Dockerfile:

## Dockerfile

- Especifica la imagen base desde la cual se construira la imagen:

FROM image:tag

- Establece el directorio de trabajo dentro del contenedor. Las instrucciones siguientes se ejecutarán en este directorio:

WORKDIR /path/to/workdir

- Copia archivos o directorios desde el sistema de archivos local al sistema de archivos del contenedor:

COPY <local> <remote>

- Ejecuta comandos durante la construcción de la imagen. Puedes usarlo para instalar paquetes, configurar el entorno.... :

RUN command example: RUN npm install

- Proporciona el comando predeterminado a ejecutar cuando el contenedor se inicia:

CMD ["executable", "param1", "param2"] example: CMD ["npm", "run", "dev"]

- Informa a Docker que la aplicación dentro del contenedor escuchará en el puerto especificado en tiempo de ejecución:

EXPOSE port

- Establece variables de entorno dentro del contenedor:

ENV key=value

- Crea un punto de montaje para almacenar datos persistentes fuera del contenedor:

VOLUME ["/data"]