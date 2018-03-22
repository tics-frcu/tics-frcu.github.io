# Instalar VirtualBox 5.2 en Ubuntu 14.04 o Mint 17

## Instalar los paquetes necesarios

Ejecutar los siguientes  comandos:

```
echo "deb http://download.virtualbox.org/virtualbox/debian trusty contrib" | sudo tee -a /etc/apt/sources.list.d/virtualbox.list
```

```
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
```

```
sudo apt-get update
```

```
sudo apt-get install virtualbox-5.2 dkms vinagre
```

## Instalar extensiones

Descargar el paquete de extensiones de: [aquí](https://download.virtualbox.org/virtualbox/5.2.8/Oracle_VM_VirtualBox_Extension_Pack-5.2.8.vbox-extpack)

En virtualbox, instalar accediendo a: Archivo -> Preferencias -> Extensiones.
Click en botón Agregar Nuevo Paquete y seleccionar el archivo descargado.

## Copiar archivos necesarios

Copiar los archivos:

* `turnkey-lamp-14.2-jessie-amd64.iso`
* `turnkey-lamp-14.2-jessie-amd64.ova`
* `ubuntu-16.04.4-server-i386.iso`

a la carpeta `~/consolidacion-2018`

Los mismos se pueden descargar de:

* [https://www.turnkeylinux.org/download?file=turnkey-lamp-14.2-jessie-amd64.ova](https://www.turnkeylinux.org/download?file=turnkey-lamp-14.2-jessie-amd64.ova)
* [https://www.turnkeylinux.org/download?file=turnkey-lamp-14.2-jessie-amd64.iso](https://www.turnkeylinux.org/download?file=turnkey-lamp-14.2-jessie-amd64.iso)
* [http://releases.ubuntu.com/16.04.2/ubuntu-16.04.4-server-i386.iso](http://releases.ubuntu.com/16.04.2/ubuntu-16.04.4-server-i386.iso)
