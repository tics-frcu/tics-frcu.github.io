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
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \ 
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

## Verificar que kubectl puede interactuar con Minikube

```
kubectl get pods --all-namespaces
```

nos debería mostrar una salida similar a:

```
NAMESPACE     NAME                                    READY   STATUS    RESTARTS   AGE
kube-system   coredns-fb8b8dccf-4dbq7                 1/1     Running   5          12d
kube-system   coredns-fb8b8dccf-bhbbg                 1/1     Running   5          12d
kube-system   etcd-minikube                           1/1     Running   2          12d
kube-system   kube-addon-manager-minikube             1/1     Running   2          12d
kube-system   kube-apiserver-minikube                 1/1     Running   2          12d
kube-system   kube-controller-manager-minikube        1/1     Running   2          12d
kube-system   kube-proxy-hbd4s                        1/1     Running   1          7h58m
kube-system   kube-scheduler-minikube                 1/1     Running   2          12d
kube-system   kubernetes-dashboard-79dd6bfc48-hqxsw   1/1     Running   0          9m59s
kube-system   storage-provisioner                     1/1     Running   5          12d
```

# Instalar Kubernetes y Minikube en otros S.O

* [https://kubernetes.io/docs/tasks/tools/install-kubectl/][Instalar kubectl]
* [https://kubernetes.io/docs/tasks/tools/install-minikube/][Instalar Minikube] 

[Instalar kubectl]: https://kubernetes.io/docs/tasks/tools/install-kubectl/

[Instalar Minikube]: https://kubernetes.io/docs/tasks/tools/install-minikube/