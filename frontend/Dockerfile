# Usamos una imagen base de Node.js
FROM node:18-alpine
RUN apk add --no-cache python3 make g++  # Solo si necesitas compilar módulos nativos

# Definir directorio de trabajo
WORKDIR /app

# Copiar archivos de package.json y package-lock.json para instalar dependencias
COPY package*.json ./

# Instalar dependencias
RUN npm install

# Copiar el resto del código
COPY . .

# Construir la aplicación (si deseas servir una versión de producción)
RUN npm run build

# Exponer el puerto en el que corre la app de Vite (usualmente 3000)
EXPOSE 3000

# Ejecutar la aplicación (en modo desarrollo o producción, según convenga)
# Para desarrollo, podrías usar:
CMD ["npm", "run", "dev"]
