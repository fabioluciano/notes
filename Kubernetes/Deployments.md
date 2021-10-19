# Deployments
* Deployments é o recurso capaz de realizar a manipulação de pods e ReplicaSets. Configurando o estado desejado de um deployment ele permite de maneira controlada a implantação/alteração do estado atual do recurso para o estado desejado.

* Deployments utiliza apiVersion: apps/v1

## Comandos úteis
 
 > Recupera deployments dos nós
 > `kubectl get deployments`

> Recupera informações sobre o deployment
> `kubectl describe deployment deployment-name`

> Cria deployment
> `kubectl create -f deployment-file-definition.yml`

> deleta deployment
> `kubectl delete deployment deployment-name`


