<!-- Curso de Docker: Fundamentos -->
# 1. Fundamentos de Docker y Contenedores para Desarrolladores
Docker se ha convertido rápidamente en una herramienta esencial para gestionar y publicar soluciones de software mediante contenedores. La esencia y punto fuerte de Docker radica en su capacidad para aislar aplicaciones, asegurando que estas funcionen de manera consistente en diferentes sistemas operativos o entornos, resolviendo así la clásica situación de "en mi máquina sí funciona".

Puedes encontrar el repositorio de este curso en  https://github.com/platzi/curso-de-docker-fundamentos cada rama puedes conseguir los archivos que se usaran al final del curso

## ¿Qué es realmente un contenedor en Docker?
Aunque pueda confundirse con máquinas virtuales, un contenedor es algo distinto: es un espacio aislado donde empaquetas toda tu solución, incluyendo dependencias y configuraciones. Esto permite que el proyecto, al transportarse de un lugar a otro, funcione exactamente igual sin importar factores externos, como el sistema operativo o ambiente.

Gracias al `docker daemon`, o el corazón de Docker, puedes gestionar eficazmente:

- Redes.
- Volúmenes.
- Imágenes previas necesarias para crear nuevos contenedores.

## ¿Qué diferencia a Docker de otros conceptos tecnológicos?
A menudo se mezclan términos como microservicios, Kubernetes y Docker, pensando equivocadamente que son sinónimos. En realidad, estas tecnologías tienen definiciones y aplicaciones particulares que, aunque participen integradas en ciertos procesos, presentan diferencias considerables entre ellas.

Docker te permite específicamente crear y gestionar contenedores individuales. Mientras que Kubernetes se centra en la gestión, orquestación y despliegue de múltiples contenedores dentro de infraestructuras más grandes. Por su parte, los microservicios describen un estilo arquitectónico en el que las aplicaciones se componen de módulos pequeños e independientes.

## ¿Qué conocimientos previos facilitan el aprendizaje de Docker?

Tener experiencia en bash o manejo de terminal y sistemas operativos basados en Linux facilitará mucho la transición al uso de Docker y sus contenedores. Experimentar comandos directamente en una terminal te dará confianza y hará que usar Docker sea más sencillo y natural.

La idea es comprender progresivamente qué es exactamente un contenedor, cómo funciona dentro del entorno Docker y cómo aprovecharlo para tus soluciones de software. Así, serás capaz de integrarlo y aplicarlo efectivamente en tus propios desarrollos.

Te invitamos a compartir en los comentarios cuáles han sido las dudas más frecuentes que has encontrado al trabajar con Docker y contenedores.