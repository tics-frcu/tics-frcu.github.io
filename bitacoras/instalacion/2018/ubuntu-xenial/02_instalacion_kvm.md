# Instalación de qemu-kvm en Ubuntu 16.04 o Mint 18

## Instalar los paquetes necesarios
```
sudo apt-get update
```

```
sudo apt-get install qemu-kvm qemu-system libvirt-bin ubuntu-vm-builder bridge-utils virt-manager
```

```
sudo usermod -a -G libvirtd $USER
```

```
sudo usermod -a -G kvm $USER
```

Reiniciar el equipo o desloguearse y volver a ingresar.
