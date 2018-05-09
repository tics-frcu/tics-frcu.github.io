# Instalar Docker Compose en Ubuntu / Mint / Debian 

## Eliminamos versiones anteriores

Verificamos si ya tenemos instalado Docker Compose

```
whereis docker-compose
```

Si existe lo eliminamos

```
sudo rm /usr/local/bin/docker-compose
```

## Descargamos e instalamos el binario de Docker Compose

```
sudo curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
```

```
sudo chmod a+rx /usr/local/bin/docker-compose
```

## Verificamos la versión instalada

```
docker-compose --version
```

