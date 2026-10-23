# Guía de instalación y configuración

## FASE 1: Preparación del entorno

Instalación de las herramientas necesarias para trabajar con Git y realizar peticiones HTTP mediante curl.

```bash
sudo apt-get install git
sudo apt -get install curl
```

Detener y eliminar los contenedores existentes de Docker para comenzar con un entorno limpio.

```bash
docker stop $(docker ps -aq)
docker rm $(docker ps -aq)
```

Descargar la imagen de Nginx con Alpine Linux, que se utilizará para desplegar el servidor web.

```bash
docker pull nginx:alpine
```

## FASE 2: Creación y ejecución del contenedor

Ejecutar un contenedor temporal de Nginx y configurar el mapeo del puerto 8080 de la máquina anfitriona al puerto 80 del contenedor.

```bash
docker run --rm -p 8080:80 nginx:alpine
```

Crear un contenedor de Nginx con el nombre `mi_web` y mantener una sesión interactiva abierta, exponiendo el servicio en el puerto 8080.

```bash
docker run -it -p 8080:80 --name mi_web nginx:alpine
```

## FASE 3: Inicio del contenedor

Iniciar el contenedor `servidor_web` para poner en funcionamiento el servicio web.

```bash
docker start servidor_web
```

## FASE 4: Verificación del servicio web

Comprobar que el servidor web responde correctamente a través del puerto 8080 utilizando curl y el navegador web.

```bash
curl localhost:8080
https://localhost:8080
```

## FASE 5: Clonación del repositorio

Clonar el repositorio de GitHub que contiene los archivos y recursos necesarios para realizar las prácticas de Docker.

```bash
git clone https://github.com/Alexxalataaa/practicas_docker.git
```
