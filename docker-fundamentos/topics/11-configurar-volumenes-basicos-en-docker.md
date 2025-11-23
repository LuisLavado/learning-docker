# Gestión de Volúmenes en Docker para Desarrollo Web

Los volúmenes en Docker brindan la posibilidad de compartir información directamente entre el equipo local y un contenedor activo, facilitando la actualización constante y eficiente de contenidos como sitios web o análisis de datos en marcha. Esta herramienta permite reflejar modificaciones instantáneamente sin detener procesos.

## ¿Qué es exactamente un volumen en Docker?

Un volumen en Docker es equivalente a una carpeta o unidad compartida entre tu computadora y un contenedor que está en ejecución. Esta función crea un puente de comunicación bidireccional, vital para proyectos que requieren una actualización continua del contenido:

- Cambios en páginas web activas.
- Integración periódica de grandes volúmenes de datos.

Es importante subrayar que esta interacción se realiza exclusivamente con contenedores activos, no con imágenes almacenadas.

## ¿Cómo implementar un volumen en un proyecto sencillo con Docker?

Una manera práctica es desplegar un sitio web localmente usando el servidor web Nginx. El procedimiento es sencillo:

1. Se crea una carpeta local llamada `sitio` que contiene archivos HTML y recursos gráficos en `assets`.
2. En la terminal, se ingresa:

- En Linux

    ```
    docker run -it --rm -d -p 8080:80 -v ./sitio:/usr/share/nginx/html/sitio --name web nginx
    ```

- En Windows: mientras en Linux se maneja "./sitio" (ruta ubuntu), en windows funciona con "disco:\ruta_de_la_carpeta_windows" ejem: "D:\cursodocker\sitio"

    ```
    docker run -it --rm -d -p 8080:80 -v D:/PROJECTS/learning-docker/projects/clase-11/sitio:/usr/share/nginx/html/sitio --name web nginx:1.0
    ```

Con este comando, se comparte directamente el contenido del directorio local sitio dentro del contenedor Docker.

- Al modificar localmente los archivos HTML, como cambiar imágenes en la propiedad `src`, los cambios aparecen inmediatamente en el navegador web al recargar la página.

## ¿Qué diferencias existen entre copiar y crear volúmenes?

Existen diferencias claves entre los comandos Docker `copy` y utilizar volúmenes:

### ¿Cuándo debes usar `COPY`?

- Proyectos estáticos, sin necesidad frecuente o continua de actualización.
- Cuando deseas mantener una copia permanente y aislada del contenido original dentro de la imagen Docker.

## ¿Cuándo es recomendable utilizar un volumen?

- Para proyectos que necesitan ser actualizados con frecuencia o mientras están corriendo.
- En casos de análisis de datos que requieren ingresar continuamente nueva información.

Cada opción ofrece beneficios según la naturaleza dinámica o estática del proyecto, siendo crucial decidir con claridad cuál método es más apropiado para tu caso particular.