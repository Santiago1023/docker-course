# la base es un debian, e instale node:20.13.
FROM node:20.13.0  

# en el contenedor que vaya a crear, cree esta carpeta y haga cd (esta expresión se refiere siempre al contenedor)
WORKDIR /usr/src/app

# ./ y . -> es para copiar todo en el directorio que estoy parado
COPY package*.json ./

# correr un comando en especifico dentro de la imagen 
# RUN para correr comandos antes de que la aplicacion sea ejecutada -> no se puede sobreescribir
RUN npm install

# copie todos los archivos que encuentre en el mismo nivel del Dockerfile, y peguelo en el WORKDIR
COPY . .

#exponer el puerto de la aplicación
EXPOSE 3000

# cmd sirve para poner a correr la aplicaciaon  -> este comando se puede sobreescrbir en tiempo de ejecución del contenedor
CMD [ "npm", "start" ]
