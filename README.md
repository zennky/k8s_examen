# Examen k8s en GKE o k3d

Los archivos *.yaml para poder levantar toda la infraestructura se encuentra en el directorio: `k8s`.

Las imagenes que muestran el funcionamiento del sistema se encuentra en el directorio: `imagenes`.

## Autor

Erick Ibañez Velasco

## Instrucciones para ejecutar el codigoCodigo a ejecutar

Se debe ejecutra codigo desde un cliente `kubectl`.

## Crear Namespace: vote
$ kubectl create ns vote
## a. vote deployment - Create a deployment: name = 'vote-deployment'
$ kubectl apply -f  k8s/deployment-vote.yml
## b. vote service - Create a new service: name = vote-service
$ kubectl apply -f  k8s/svc-vote.yaml
## c. redis deployment - Create new deployment, name: 'redis-deployment'
$ kubectl apply -f  k8s/deployment-redis.yml
## d. redis service - New Service, name = 'redis'
$ kubectl apply -f  k8s/svc-redis.yaml
## e. worker deploy - Create new deployment. name: 'worker'
$ kubectl apply -f  k8s/deployment-worker.yml
## f. db deploy - Create new deployment. name: 'db-deployment'
$ kubectl apply -f  k8s/deployment-db.yml
## g. db service - Create new service: 'db'
$ kubectl apply -f  k8s/svc-db.yaml
## h. result deploy - Create new deployment, name: 'result-deployment'
$ kubectl apply -f  k8s/deployment-result.yml
## i. result service -  - Create new service: 'result'
$ kubectl apply -f  k8s/svc-result.yaml
