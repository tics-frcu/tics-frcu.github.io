# Instalar Docker Machine en Ubuntu / Mint / Debian 

## Eliminamos versiones anteriores

Verificamos si ya tenemos instalado Docker Machine

```
whereis docker-machine
```

Si existe, lo eliminamos

```
sudo rm `whereis pg_backup_rotated.sh` 2> /dev/null
```

## Descargamos e instalamos el binario de Docker Machine

```
sudo curl -L https://github.com/docker/machine/releases/download/v0.14.0/docker-machine-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-machine
```

```
sudo chmod a+rx /usr/local/bin/docker-machine
```

## Verificamos la versión instalada

```
docker-machine version
```

