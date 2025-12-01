# 🐳 Docker Learning Repository

Bienvenido a mi repositorio de aprendizaje de **Docker**.  
Aquí documento paso a paso todo lo que estoy aprendiendo, desde los fundamentos hasta conceptos avanzados, acompañado de **proyectos prácticos**, apuntes en **Markdown**, ejemplos y comandos reales.

El objetivo de este repo es:

- Servir como **guía de estudio personal**.
- Ser una **referencia para otros desarrolladores** que quieran aprender Docker desde cero.
- Tener un espacio donde combinar teoría + práctica con microproyectos que refuerzan cada lección.

---

## 📚 Tabla de Contenidos

- [Acerca de este repositorio](#acerca-de-este-repositorio)
- [Estructura de Carpetas](#-estructura-de-carpetas)
- [Curso 1: Docker - Fundamentos](#-curso-1-docker---fundamentos)
- [Curso 2: Docker Avanzado](#-curso-2-docker-avanzado)
- [Proyectos Prácticos](#-proyectos-prácticos)
- [Requisitos](#-requisitos)
- [Cómo usar este repositorio](#-cómo-usar-este-repositorio)
- [Comandos esenciales de Docker](#-comandos-esenciales-de-docker)
- [Recursos recomendados](#-recursos-recomendados)
- [Licencia](#-licencia)

---
<a id="acerca-de-este-repositorio"></a>
## 📦 Acerca de este repositorio

Este repositorio contiene:

- Notas detalladas de cada clase en **Markdown**  
- Ejemplos reales y explicados  
- Mini–proyectos de práctica para cada módulo  
- Buenas prácticas que he recopilado mientras aprendo Docker  

La idea es que evolucione como una **documentación viva**.

---

## 📁 Estructura de Carpetas

```
docker-learning/
│
├── docker-fundamentos/
├── docker-avanzado/
├── proyectos/
│ ├── proyecto-01/
│ ├── proyecto-02/
│ └── ...
│
└── README.md
```

`docker-fundamentos` y `docker-avanzado` tienen su propia estructura de carpetas. Y a medida que cresca éste repositorio, se añadirán más `proyectos`.

---

## 🐳 Curso 1: Docker - Fundamentos

Ya completado ✔️  

En esta sección podrás encontrar mis apuntes, comandos explicados, diagramas y proyectos prácticos.

📄 **Notas del curso:**  
👉 [Ver apuntes del Curso de Docker Fundamentos](./docker-fundamentos/README.md)

📌 Temas cubiertos:

- ¿Qué es Docker y por qué usarlo?
- Contenedores vs Máquinas Virtuales  
- Imágenes y contenedores  
- Dockerfile  
- Volúmenes  
- Redes en Docker  
- Docker Hub  
- Docker Compose básico  
- Buenas prácticas  

---

## 🚀 Curso 2: Docker Avanzado

*(Aún por comenzar)*

Esta sección contendrá:

- Docker Compose avanzado  
- Multi–stage builds  
- Optimización de imágenes 
- Orquestación  
- Variables de entorno y secretos  
- Debugging en contenedores  
- Patrones avanzados para entornos reales  

📄 **Notas del curso:**  
👉 [Ver apuntes del Curso de Docker Avanzado](./docker-avanzado/README.md)

---

## 🧪 Proyectos Prácticos

Cada módulo contiene mini–proyectos diseñados para reforzar lo aprendido.

<!-- Ejemplos:

- Crear una imagen desde cero  
- Servidor Nginx personalizado  
- API simple en Node / Python dentro de Docker  
- Volúmenes con persistencia real  
- Redes entre contenedores  
- Docker Compose con varios servicios  
- Multi–stage builds para producción   -->

👉 [Ver proyectos del Curso de Docker Fundamentos](./proyectos/)  
👉 (Se agregarán más en el curso avanzado)

---

## 🛠 Requisitos

- Docker Desktop / Docker Engine  
- Docker Compose  
- Git  
- Editor de código (VSCode recomendado)  

---

## 💡 Cómo usar este repositorio

1. Clona el repositorio:

```bash
git clone https://github.com/LuisLavado/learning-docker.git
```

2. Navega entre las carpetas y revisa los apuntes en Markdown.

3. Ejecuta los proyectos prácticos siguiendo las instrucciones en cada carpeta.

4. Usa este repositorio como referencia mientras trabajas tus propios contenedores.

## 🔧 Comandos esenciales de Docker

```
docker ps              # Listar contenedores activos  
docker ps -a           # Listar todos  
docker images          # Listar imágenes  
docker build -t nombre .  
docker run -d -p 80:80 nombre  
docker exec -it <id> bash  
docker stop <id>  
docker rm <id>  
docker-compose up -d  
docker-compose down  
```

## 📘 Recursos recomendados

- Documentación oficial: https://docs.docker.com

- Play with Docker: https://labs.play-with-docker.com

- Docker Hub: https://hub.docker.com

- Cursos de Platzi / Udemy / YouTube

## 📄 Licencia

MIT License — libre para usar, modificar y compartir.
