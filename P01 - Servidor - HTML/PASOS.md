# PASO a PASO

## FASE 1

Instalar git y curl
```bash
sudo apt-get install git
sudo apt -get install curl
```

Limpieza de docker
```bash
docker stop $(docker ps -aq)
docker rm $(docker ps -aq)
```

Descargar imagen
```bash
docker pull nginx:alpine
```


## FASE 2

Contenedor temporal
``` bash
docker run --rm -p 8080:80 nginx:alpine
```

Crear contenedor
```bash
docker run -it -p 8080:80 --name mi_web nginx:alpine
```


## FASE 3

Levantar contenedor
``` bash
docker start servidor_web
```


## FASE 4

Comprobar funcionamiento del mapeo de puerto
```bash
curl localhost:8080
https://localhost:8080
```


## FASE 5

Clonar contenedor de la máquina real
``` bash
git clone https://github.com/Alexxalataaa/practicas_docker.git
```
