# 🐳 Curso de Docker: Fundamentos

Este directorio contiene mis apuntes y ejercicios del curso **“Curso de Docker: Fundamentos”**.  
Aquí encontrarás resúmenes de cada clase, comandos importantes y proyectos prácticos que puedo usar como referencia rápida.

---

## 📚 Tabla de contenidos

- [Descripción del curso](#-descripción-del-curso)
- [Requisitos](#-requisitos)
- [Estructura de archivos](#-estructura-de-archivos)
- [Clases del curso](#-clases-del-curso)
- [Proyectos prácticos](#-proyectos-prácticos)
- [Comandos útiles de referencia](#-comandos-útiles-de-referencia)

---

## 🧾 Descripción del curso

En este curso aprendí a:

- Entender qué es Docker y por qué es útil para desarrolladores.
- Crear y gestionar **imágenes** y **contenedores**.
- Trabajar con **Docker Desktop**, **Dockerfile**, **volúmenes** y **redes**.
- Publicar imágenes en **Docker Hub**.
- Orquestar contenedores con **Docker Compose**.
- Aplicar buenas prácticas en entornos de desarrollo.

---

## 🛠 Requisitos

- Docker instalado (Docker Desktop o Docker Engine).
- Git.
- Editor de texto / IDE (por ejemplo, VS Code).
- Conocimientos básicos de terminal.

---

## 📁 Estructura de archivos

> Ajusta los nombres de archivo si usas otra convención.

```text
curso-docker-fundamentos/
│
├── 01-fundamentos-de-docker-y-contenedores.md
├── 02-diferencias-maquinas-virtuales-vs-contenedores.md
├── 03-instalacion-docker-windows-mac-linux.md
├── 04-uso-de-docker-desktop.md
├── 05-comandos-esenciales-de-docker.md
├── 06-contenedor-web-nginx-en-code.md
├── 07-creacion-de-imagenes-con-docker.md
├── 08-gestion-de-contenedores.md
├── 09-gestion-de-imagenes-y-contenedores.md
├── 10-admin-contenedores-practicas-esenciales.md
├── 11-despliegue-api-flask-en-docker.md
├── 12-gestion-de-volumenes.md
├── 13-redes-en-docker.md
├── 14-publicacion-imagenes-docker-hub.md
├── 15-exploracion-de-contenedores-comandos-basicos.md
├── 16-exportar-importar-imagenes-cli.md
└── 17-docker-compose-despliegue-frontend-backend.md
```

## 🎓 Clases del curso

Cada clase tiene su propio archivo Markdown con resumen, comandos y notas personales.

**1. [Fundamentos de Docker y Contenedores para Desarrolladores](./topics/01-fundamentos-de-docker-y-contenedores.md)**

**2. [Diferencias entre Máquinas Virtuales y Contenedores Docker](./topics/02-diferencias-maquinas-virtuales-vs-contenedores.md)**

**3. [Instalación de Docker en Windows, Mac y Linux](./topics/03-instalacion-docker-windows-mac-linux.md)**

**4. [Exploración y Uso de Docker Desktop para Desarrolladores](./topics/04-uso-de-docker-desktop.md)**

**5. [Comandos esenciales de Docker: Uso y documentación](./topics/05-comandos-esenciales-de-docker.md)**

**6. [Creación de Contenedores Web con Docker y Nginx en VS Code](./topics/06-contenedor-web-nginx-en-code.md)**

**7. [Creación de Imágenes con Docker](./topics/07-creacion-de-imagenes-con-docker.md)**

**8. [Gestión de Contenedores Docker: Comandos y Docker Desktop](./topics/08-gestion-de-contenedores.md)**

**9. [Gestión de Imágenes y Contenedores en Docker](./topics/09-gestion-de-imagenes-y-contenedores.md)**

**10. [Administración de Contenedores Docker: Comandos y Prácticas Esenciales](./topics/10-admin-contenedores-practicas-esenciales.md)**

**11. [Despliegue de API Flask en Docker paso a paso](./topics/11-despliegue-api-flask-en-docker.md)**

**12. [Gestión de Volúmenes en Docker para Desarrollo Web](./topics/12-gestion-de-volumenes.md)**

**13. [Redes en Docker: Configuración y Gestión Eficiente de Contenedores](./topics/13-redes-en-docker.md)**

**14. [Publicación de Imágenes Docker en Docker Hub](./topics/14-publicacion-imagenes-docker-hub.md)**

**15. [Exploración de Contenedores Docker y sus Comandos Básicos](./topics/15-exploracion-de-contenedores-comandos-basicos.md)**

**16. [Exportación e importación de imágenes Docker con comandos CLI](./topics/16-exportar-importar-imagenes-cli.md)**

**17. [Despliegue de Aplicaciones con Docker Compose: Frontend y Backend](./topics/17-docker-compose-despliegue-frontend-backend.md)**

## 🧪 Proyectos prácticos

Los proyectos relacionados con este curso se encuentran en la carpeta proyectos/.

Ejemplos (puedes adaptar la lista a lo que tengas creado):

- Proyecto 01 – Contenedor Web con Nginx  
  Carpeta: `proyectos/proyecto-01/`
  - Servir un sitio estático con Nginx dentro de un contenedor.
  - Configuración básica de puertos y redes.

- Proyecto 02 – API Flask en Docker  
  Carpeta: `proyectos/proyecto-02/`
  - Dockerizar una API sencilla en Flask.
  - Uso de volúmenes para recarga en desarrollo.

## 🧾 Comandos útiles de referencia

```
# Ver contenedores
docker ps
docker ps -a

# Ver imágenes
docker images

# Construir una imagen
docker build -t nombre-imagen .

# Ejecutar un contenedor
docker run -d -p 8080:80 --name mi-contenedor nombre-imagen

# Entrar a un contenedor
docker exec -it mi-contenedor bash

# Detener y eliminar contenedores
docker stop mi-contenedor
docker rm mi-contenedor

# Docker Compose
docker compose up -d
docker compose down
```
