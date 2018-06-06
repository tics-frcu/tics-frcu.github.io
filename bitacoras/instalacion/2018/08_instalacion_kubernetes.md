# Instalar Kubernetes (con minikube) en Ubuntu / Mint / Debian 

## Eliminamos versiones anteriores

Si ya tenemos instalados kubectl y minikube, los eliminamos

```
sudo rm `whereis kubectl` 2> /dev/null
```

```
sudo rm `whereis minikube` 2> /dev/null
```

## Descargamos e instalamos los binarios de ambas herramientas

```
curl -Lo kubectl https://storage.googleapis.com/kubernetes-release/release/v1.10.0/bin/linux/amd64/kubectl \ 
&& chmod +x kubectl \
&& sudo mv kubectl /usr/local/bin/
```

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
&& chmod +x minikube \
&& sudo mv minikube /usr/local/bin/
```

## Verificamos las versiones instaladas

```
kubectl version
```


```
minikube version
```

## Creamos e iniciamos el cluster kubernetes de prueba

```
minikube start
```

## Para acceder al Dashboard del cluster utilizar

```
minikube dashboard
```

## Para detener el cluster utilizar

```
minikube stop
```
