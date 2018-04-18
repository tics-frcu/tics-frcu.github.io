# Instalar vagrant en Ubuntu / Debian de 64 bits

## Descargar e instalar vagrant

```
mkdir vagrant; cd vagrant/
```

```
wget https://releases.hashicorp.com/vagrant/2.0.3/vagrant_2.0.3_x86_64.deb
```

```
 sudo dpkg -i vagrant_2.0.3_x86_64.deb
```

```
 cd ..; rm -rf vagrant
```

Instalamos paquetes para poder exportar deirectorios vía NFS

```
sudo apt-get install nfs-kernel-server nfs-common 
```

Reiniciar el equipo o desloguearse y volver a ingresar.

## Descargar las boxes necesarias para el laboratorio

```
vagrant box add ubuntu/trusty64 
```


## Buscar otras boxes

Se pueden descargar otras boxes desde:

* https://atlas.hashicorp.com/boxes/search
* https://github.com/phusion/open-vagrant-boxes
