# Instalar VirtualBox 5.x en Ubuntu 16.04 o Mint 18

## Instalar los paquetes necesarios

1. `echo "deb http://download.virtualbox.org/virtualbox/debian xenial contrib" | sudo tee -a /etc/apt/sources.list.d/virtualbox.list`
2. `wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -`
3. `sudo apt-get update`
4. `sudo apt-get install virtualbox-5.2 dkms vinagre`

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

* https://www.turnkeylinux.org/download?file=turnkey-lamp-14.2-jessie-amd64.ova
* https://www.turnkeylinux.org/download?file=turnkey-lamp-14.2-jessie-amd64.iso
* http://releases.ubuntu.com/16.04.2/ubuntu-16.04.4-server-i386.iso

