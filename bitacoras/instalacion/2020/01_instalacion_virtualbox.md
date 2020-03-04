# Instalar VirtualBox 6.0 en Ubuntu 18.04 / Mint 19

## Instalar los paquetes necesarios

Ejecutar los siguientes  comandos:

```
echo "deb http://download.virtualbox.org/virtualbox/debian bionic contrib" | sudo tee -a /etc/apt/sources.list.d/virtualbox.list
```

```
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
```

```
sudo apt update
```

```
sudo apt install virtualbox-6.1 dkms vinagre
```

## Instalar extensiones

Descargar el paquete de extensiones de: [aquí](https://download.virtualbox.org/virtualbox/6.1.4/Oracle_VM_VirtualBox_Extension_Pack-6.1.4.vbox-extpack)

En virtualbox, instalar accediendo a: Archivo -> Preferencias -> Extensiones.
Click en botón Agregar Nuevo Paquete y seleccionar el archivo descargado.

## Copiar archivos necesarios

Copiar los archivos:

* `ubuntu-18.04.4-server-amd64.iso`
* `turnkey-lamp-15.1-stretch-amd64.iso`
* `turnkey-lamp-15.1-stretch-amd64.ova`

a la carpeta `~/consolidacion-2020`

Los mismos se pueden descargar de:

* [http://cdimage.ubuntu.com/releases/18.04.4/release/ubuntu-18.04.4-server-amd64.iso](http://cdimage.ubuntu.com/releases/18.04.4/release/ubuntu-18.04.4-server-amd64.iso)
* [https://www.turnkeylinux.org/download?file=turnkey-lamp-15.1-stretch-amd64.iso](https://www.turnkeylinux.org/download?file=turnkey-lamp-15.1-stretch-amd64.iso)
* [https://www.turnkeylinux.org/download?file=turnkey-lamp-15.1-stretch-amd64.ova](https://www.turnkeylinux.org/download?file=turnkey-lamp-15.1-stretch-amd64.ova)

