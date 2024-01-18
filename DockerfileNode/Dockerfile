# Usa la última imagen oficial de Node.js como base
FROM node:20

# Establece el directorio de trabajo en el contenedor
WORKDIR /usr/src/app

# Copia los archivos de la aplicación al contenedor
COPY hello.js package.json /usr/src/app/

# Instala las dependencias de la aplicación
RUN npm install

# Expone el puerto en el que la aplicación se ejecutará
EXPOSE 3000

# Define el comando predeterminado para iniciar la aplicación
CMD ["npm", "start"]