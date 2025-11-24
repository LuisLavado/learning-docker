# Usar una imagen oficial de Node como imagen base
FROM node:18

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo 'package.json' y 'package-lock.json' (si está disponible)
COPY package*.json ./

# Instalar dependencias del proyecto
RUN npm install

# Copiar todos los archivos locales en el contenedor
COPY . .

# Construir la aplicación en modo producción
RUN npm run build

# Exponer el puerto que Next.js utilizará
EXPOSE 3000

# Comando para ejecutar la aplicación
CMD ["npm", "start"]
