# Instalar cluster Kubernetes (con minikube) en Ubuntu / Mint / Debian 

## Requisitos previos

Tener instalado y funcionando Docker.

## Eliminamos versiones anteriores

Si ya tenemos instalados kubectl y/o kind, los eliminamos con

```
sudo rm `whereis kubectl` 2> /dev/null
```

```
sudo rm `whereis kind` 2> /dev/null 
```

## Descargamos e instalamos los binarios de ambas herramientas

```
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \ 
&& chmod +x kubectl \
&& sudo mv kubectl /usr/local/bin/ \
&& kubectl completion bash | sudo tee -a /etc/bash_completion.d/kubectl
```

```
curl -Lo kind https://kind.sigs.k8s.io/dl/v0.7.0/kind-$(uname)-amd64 \
&& chmod +x kind \
&& sudo mv kind /usr/local/bin/
```

## Verificamos las versiones instaladas

```
kubectl version
```

```
kind version
```

## Creamos e iniciamos el cluster kubernetes de prueba

Creamos el cluster

```
curl -Lo kind-cluster.yaml https://tics-frcu.github.io/bitacoras/instalacion/2020/kind-cluster.yaml \
&& kind create cluster --config kind-cluster.yaml 
```

Verificamos que el cluster está funcinando con:
```
kubectl get nodes
```

un poco más de información con
```
kubectl get nodes -o wide
```
Definimos un ingress Nginx para el cluster con:

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/master/deploy/static/provider/kind/deploy.yaml
```





