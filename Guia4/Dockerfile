# Usa la imagen oficial de Node.js 20 con Alpine
# Alpine es una distribución de Linux muy ligera, lo que resulta en imágenes más pequeñas
FROM node:20-alpine

# Establece el directorio de trabajo en el contenedor
# Todos los comandos siguientes se ejecutarán desde este directorio
WORKDIR /app

# Copia los archivos package.json y package-lock.json (si está disponible)
# Esto se hace antes de copiar todo el código para aprovechar la caché de Docker
# Si estos archivos no han cambiado, Docker reutilizará las capas almacenadas en caché
COPY package*.json ./


# Instala las dependencias del proyecto
RUN npm install

# Copia los archivos y carpetas del proyecto al directorio de trabajo del contenedor
# Esto incluye tu código fuente, configuraciones, etc.
COPY . .

# Compila la aplicación para producción
# Este paso es necesario si estás usando Vue CLI o necesitas un paso de construcción
RUN npm run build

# Expone el puerto en el que se ejecutará la aplicación
# Esto es más que nada documentativo, ya que no publica realmente el puerto
EXPOSE 8080

# Define el comando para ejecutar la aplicación
# Esto iniciará tu aplicación Vue cuando el contenedor se inicie
CMD ["npm", "run", "serve"]
