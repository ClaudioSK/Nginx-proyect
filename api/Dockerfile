FROM node:14-alpine

# Establece el directorio de trabajo
WORKDIR /app

# Copia los archivos de configuración de npm
COPY package*.json ./

# Instala curl y las dependencias de npm
RUN apk add --no-cache curl && npm install

# Copia el resto del código fuente
COPY . .

# Construye la aplicación
RUN npm run build

# Expone el puerto 3000
EXPOSE 3000

# Define el comando de inicio
CMD ["npm", "run", "start:prod"]