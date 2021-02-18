# Creación de blogs con Jekyll y GutHub Pages

Creando una página de blog con Jekyll y GitHub.

## Preparando la máquina

Esto lo podemos hacer en cualquier máquina, debemos tener instaladas las herramientas de github, docker y docker-compose.

## Preparando nuestro repositorio

Tenemos que tener creado en GitHub un repositorio con nuestro nombre seguido del gominio github.io

![captura1](https://github.com/vaeruiz/iaw-jekyll/blob/main/imagenes/captura1.png?raw=true)

Con el repositorio creado, lo clonamos en la máquina con la que estamos trabajando.

## Creando nuestro sitio

Cuando se haya clonado entramos y lanzamos el contenedor de Jekyll que nos creará la infraestructura de nuestro blog.

> docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog

Se nos creará un nuevo directorio llamado blog, debemos mover todo el contenido de ese directorio a la raíz del directorio clonado. Podemos hacerlo con un mv

> mv blog/* ./

## Creando posts

Antes de subir nuestra página, aprenderemos a manejar los posts.

Con todos los pasos anteriores hechos, a la hora de crear/editar posts tenemos que hacer lo siguiente:

En la carpeta _posts se almacenan todos los posts de nuestro sitio, si lo desplegamos encontraremos un archivo de ejemplo bajo el nombre de

>2021-02-18-welcome-to-jekyll.markdown

Los posts se escriben en lenguaje markdown, tienen una estructura que siempre se debe respetar y que podemos encontrar en ese post de ejemplo.

El título consta de:

- Año en el que se ha creado el post.
- Mes en el que se ha creado.
- Día del mes en el que se ha creado.
- Título del post

Todo esto seguido de la extensión markdown.

Dentro del archivo encontraremos las secciones correspondientes a el título que le podemos poner, fecha de redacción, y categoría.

A continuación podemos empezar a redactar el contenido de nuestro post utilizando el lenguaje de markdown (siempre lo utilizaremos, tanto para la redacción como para añadir imágenes, videos, y todos los elementos que nos permite MD)

## Publicando nuestro sitio

Para subir nuestro blog a GutHub y que esté disponible tenemos que hacer git add --all, después realizar el commit correspondiente, y finalmente un push.

>git add --all

>git commit -m "Comentario para el commit"

>git push

Después de esto, esperamos un rato a que nuestro blog se configure con todo, cuando todo esté listo podremos acceder a nuestro blog a través del nombre que hemos puesto en el repositorio.

## Imágenes y recursos multimedia

Todo el contenido multimedia que queramos añadir a nuestros posts debe estar previamente almacenado en un directorio de nuestro repositorio, para adjuntar, por ejemplo, una foto, tenemos que utilizar la url de la foto una vez que esté en el repositorio, ejemplo 

```
![imagen](https://github.com/vaeruiz/iaw-jekyll/blob/main/imagenes/captura1.png?raw=true)
```
