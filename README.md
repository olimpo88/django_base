# Django Base
Base para iniciar un proyecto con django y docker


# Cómo usar
- Install docker y docker-compose
- Clonar el proyecto ```git clone git@github.com:olimpo88/django_base.git```
- Ingresar al directorio de docker ```cd django_base/docker/```
- Crear la imagen ```docker build -t base_django:0.1 .```
- Volver a la raiz del proyecto ```cd ..```
- Editar el archivo docker-compose.yml y configurar las variables de entorno a nuestro gusto ```nano docker-compose.yml```
- Iniciar: ```docker-compose up```


