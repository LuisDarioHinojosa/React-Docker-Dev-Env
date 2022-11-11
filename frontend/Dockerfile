# parametros que puedes cambiar :)
# la imagen en la que se basa para construir el contenedor 
ARG IMAGE=node 

# usar esta imagen de docker como template
FROM ${IMAGE}

# el directorio raiz dentro del contendor 
ARG INTERNAL_WORKSPACE=/frontend_app

# definir el directorio interno del contenedor
WORKDIR ${INTERNAL_WORKSPACE}

COPY package.json .

RUN npm install

# el directorio que el contendor comparte con tu computadora (para que lo puedas editar)
ARG EXTERNAL_BINDMOUNT=/code 

# mete tu codigo al contendor
COPY ${EXTERNAL_BINDMOUNT} .

EXPOSE 3000

CMD [ "npm", "start" ]