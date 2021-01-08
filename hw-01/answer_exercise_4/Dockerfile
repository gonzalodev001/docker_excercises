#Descargamos la imagen nginx especificando la versión.
FROM nginx:1.19.3

#Le indicamos el directorio de nuestro contedor donde se copiarán los archivos.
WORKDIR /usr/share/nginx/html

#Le indicamos de donde se copiara y hacia donde copiara.
COPY . .

#Comprobará si el servicio esta funcionando o por el contrario existe un problema
HEALTHCHECK --interval=45s --timeout=5s --start-period=15s --retries=2 CMD curl --fail http://localhost || 1

