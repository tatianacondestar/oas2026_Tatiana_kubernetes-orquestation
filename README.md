# Laboratorio Kubernetes - NGINX Deployment

## Descripción

Este laboratorio consiste en desplegar una aplicación web utilizando Kubernetes.
Se implementaron los recursos principales como Deployment, Pods, Service, ConfigMap y Secret.

La aplicación utilizada es un servidor web **NGINX**.

## Tecnologías utilizadas

* Kubernetes
* Minikube
* Kubectl
* Nginx

## Archivos del proyecto

* deployment.yaml → define el Deployment y los Pods
* service.yaml → expone la aplicación mediante NodePort
* configmap.yaml → almacena configuración
* secret.yaml → almacena datos sensibles

## Pasos ejecutados

### Crear namespace

kubectl create namespace laboratorio

### Desplegar recursos

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f configmap.yaml
kubectl apply -f secret.yaml

### Verificar recursos

kubectl get all -n laboratorio

## Resultado

Se desplegó correctamente un Deployment con 2 Pods de NGINX accesibles mediante un Service NodePort.

## Autor

Tatiana

