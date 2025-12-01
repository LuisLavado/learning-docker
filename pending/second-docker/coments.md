Para los que siguen teniendo problemas a la hora de crear el volumen:

Yo ocupe los recursos de la clase 6, por cierto y en Windows al menos lo resolví de esta manera

De hecho cree el volumen sobre la imagen previamente creada sitioweb

$ docker run -it --rm -d -p 8080:80 -v C:/Users/OneDrive/Documentos/practicas/docker/sitio:/usr/share/nginx/html/sitio --name web sitioweb
```Si lo ven lo único que hice fue pegar la ruta del directorio que estamos usando **"C:/Users/OneDrive/Documentos/practicas/docker/sitio"** en lugar de **"./sitio"**

De hecho en algún otro comentario, ya se da esta solución, lo pongo algo mas ejemplificado por si es de ayuda