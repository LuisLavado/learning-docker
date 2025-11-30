# Exportación e importación de imágenes Docker con comandos CLI

## Exportar una imagen de Docker

Para exportar una imagen Docker usamos el comando `docker save`:

```
docker save <nombreImagen> > <nombreArchivo>.rar
```

Éste comando permite guardar una imagen a un archivo.rar

Ejemplo:

```
docker save luislavado/linktree > linktree.rar
```

En el caso de linux puedes probar:

```
docker save -o <nombreArchivo.tar> <nombreImagen>
```

__Descripción__: Permite guardar una o más imágenes a un archivo tar. Ejemplo

```
ocker save -o ubuntu.tar ubuntu:latest
```
Este comando guarda la imagen de Ubuntu con la etiqueta "latest" en un archivo tar llamado ubuntu.tar.

Puedes compartir el archivo.rar a uno de tus compañeros, para que éste realice la importación.

## Importar una imagen de docker

Para exportar una imagen Docker usamos el comando `docker load`:

```
docker load <nombreImagen> > <nombreArchivo>.rar
```


Descripción: Permite cargar una imagen desde un archivo tar.
Uso: docker load -i <nombre-de-archivo.tar>
Ejemplo: docker load -i ubuntu.tar
Este comando carga una imagen desde el archivo ubuntu.tar al sistema local de Docker.
Estos comandos son muy útiles para compartir imágenes entre diferentes máquinas o para hacer backups de tus imágenes locales.