$ docker pull nginx:1.19.3
Con este comando descargamos la imagen de nginx, indicando la versión que queremos nginx:1.19.3

$  docker run -d -p 3000:80 --name server_nginx -v $(pwd):/usr/share/nginx/html nginx:1.19.3
Al ejecutar este comando iniciamos el contenedor con las siguientes características -d para que 
corra en modo demon o attach, -p le asignamos un puerto para ser accesible, --name le asignamos un nombre a nuestra instancia, -v para persistir y copiar los archivos desde nuestro directorio de la pc en la que nos encontramos, los : nos indica hacia donde queremos copiar dentro de un directorio del contenedor, que nos indica nginx /usr/share/nginx/html para que corran nuestros archivos, en este caso copiamos el archivo index.html.