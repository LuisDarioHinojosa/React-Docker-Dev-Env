# parametros que puedes cambiar :)
# la imagen en la que se basa para construir el contenedor 
ARG IMAGE=node 

# usar esta imagen de docker como template
FROM ${IMAGE}
# definir el directorio interno del contenedor

# el directorio raiz dentro del contendor 
ARG INTERNAL_WORKSPACE=/backend_app

WORKDIR ${INTERNAL_WORKSPACE}

COPY package.json .

RUN npm install

# el directorio que el contendor comparte con tu computadora (para que lo puedas editar)
#ARG EXTERNAL_BINDMOUNT=/code 

# mete tu codigo al contendor
#COPY ${EXTERNAL_BINDMOUNT} .

EXPOSE 80

CMD ["npm", "start"]