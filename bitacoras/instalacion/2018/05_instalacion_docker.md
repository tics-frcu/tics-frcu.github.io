# Instalar Docker en Ubuntu / Mint / Debian 

## Eliminamos versiones anteriores

```
sudo apt-get remove docker docker-engine docker.io
```

## Instalar los paquetes necesarios

```
sudo apt-get update
```

```
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
```

## Agregar el repositorio de Docker

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

En Ubuntu

```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

En linux Mint 18.x

```
sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'
```

Actualizamos la lista de paquetes

```
sudo apt-get update
```

## Instalar Docker

```
sudo apt-get install docker-ce
```

Agregamos a nuestro usuario al grupo Docker

```
sudo usermod -aG docker $USER
```


Reiniciar el equipo y volver a ingresar.


## Verificar que docker funciona

Corremos un container de prueba

```
docker run hello-world
```

## (Opcional) Descargar las imagenes para las prácticas

```
docker pull ubuntu:14.04
```

```
docker pull nginx:1.9
```

```
docker pull turnkeylinux/lamp-14.1
```
