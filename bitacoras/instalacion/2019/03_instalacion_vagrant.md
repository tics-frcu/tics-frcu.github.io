# Instalar vagrant en Ubuntu / Debian de 64 bits

## Descargar e instalar vagrant

```
mkdir vagrant; cd vagrant/
```

```
wget https://releases.hashicorp.com/vagrant/2.2.4/vagrant_2.2.4_x86_64.deb
```

```
 sudo dpkg -i vagrant_2.2.4_x86_64.deb
```

```
 cd ..; rm -rf vagrant
```

Instalamos paquetes para poder exportar directorios vía NFS

```
sudo apt-get install nfs-kernel-server nfs-common 
```

Reiniciar el equipo o desloguearse y volver a ingresar.

## Descargar las boxes necesarias para el laboratorio

```
vagrant box add ubuntu/bionic64 
```

## Buscar otras boxes

Se pueden descargar otras boxes desde:

* https://app.vagrantup.com/boxes/search

