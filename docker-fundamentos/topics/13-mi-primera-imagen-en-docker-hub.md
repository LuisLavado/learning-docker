# Publicación de Imágenes Docker en Docker Hub

Publicar tus imágenes Docker locales en Docker Hub permite compartirlas fácilmente con personas en diferentes partes del mundo. Utilizando esta plataforma, puedes convertir tus archivos locales en recursos disponibles públicamente, muy práctico para entornos educativos, colaborativos o productivos. Aprende claramente cómo subir tus imágenes con sencillos comandos y buenas prácticas a seguir.

## ¿Qué es Docker Hub y para qué sirve?

Docker Hub es una plataforma diseñada para alojar imágenes Docker en línea. La utilidad principal es compartir tus imágenes locales para que otras personas puedan descargarlas y desplegarlas como contenedores en sus propios entornos. Este servicio resulta especialmente útil cuando:

- Quieres mostrar un sitio web a compañeros o al público general.
- Colaborar en proyectos con otros equipos.
- Implementar imágenes para uso productivo en diversos entornos.

Es sencillo utilizar esta plataforma para compartir y mantener actualizados tus proyectos.

## ¿Cómo subir una imagen local a Docker Hub?

Para subir una imagen Docker a Docker Hub, primero asegúrate de haber creado una cuenta en Docker Hub y utilizar tu nombre de usuario para etiquetar adecuadamente tu imagen. Sigue estos pasos:

### Paso 1: Acceder desde la terminal

Abre tu terminal o Docker Desktop y escribe el comando para iniciar sesión:

```
docker login
```

Luego, ingresa tus credenciales correspondientes a tu cuenta de Docker Hub (nombre de usuario y contraseña).

### Paso 2: Etiquetar tu imagen debidamente

Es necesario seguir una sintaxis específica para etiquetar la imagen correctamente antes de subirla a Docker Hub. Usa el siguiente comando general:

```
docker build -t tu_nombre_usuario/nombre_imagen:versión .
```

Ejemplo práctico:

```
docker build -t AminEspinosa/linkthree:latest .
```

Esto garantiza que Docker reconozca adecuadamente la cuenta de usuario a la que subirás dicha imagen.

### Paso 3: Subir la imagen al repositorio

Una vez etiquetada correctamente, sube tu imagen escribiendo el comando:

```
docker push tu_nombre_usuario/nombre_imagen:versión
```

Por ejemplo:

```
docker push AminEspinosa/linkthree:latest
```

Dependiendo del tamaño de la imagen y la velocidad de tu conexión, este proceso puede durar desde algunos segundos hasta varios minutos.

## ¿Cómo descargar y utilizar una imagen pública de Docker Hub?

Cuando alguien más, como Juan, desee descargar tu imagen Docker en su equipo local, solo necesitará ejecutar el comando:

```
docker run --name nombreContenedor --rm -it -p 8080:80 nombre_usuario/nombre_imagen:versión
```

En el caso de este ejemplo específico:

```
docker run --name nombreContenedor --rm -it -p 8080:80 AminEspinosa/linkthree:latest
```

Si la imagen no existe en su entorno local, Docker automáticamente la descargará desde Docker Hub.

### Recomendaciones finales para imágenes públicas

Es importante documentar claramente en la descripción de tu imagen en Docker Hub qué hace esta imagen específicamente. Incluye información útil como la URL de acceso principal, operaciones clave o puertos utilizados. Esto facilitará enormemente su uso a otras personas interesadas.

Al descargar y ejecutar imágenes, permanece atento a los datos que se presentan en tu consola o terminal. Esto proporciona información valiosa sobre rutas, puertos y otras actividades relacionadas con la ejecución del contenedor en tu equipo.

## Lecturas recomendadas

__🔗__[Cómo crear tu cuenta en Docker Hub](https://platzi.com/blog/como-crear-tu-cuenta-en-docker-hub/)

🔗[Cómo utilizar registros privados de Docker](https://platzi.com/blog/como-utilizar-registros-privados-de-docker/)