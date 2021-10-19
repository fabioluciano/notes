# ReplicaSet
* ReplicaSet é um conjunto de pods que possibilita a execução e controle de réplicas. Visando garantir a disponibilidade de um número especificado/desejado de pods.

* ReplicaSet utiliza apiVersion: apps/v1

## Comandos úteis
 
 > Recupera replicaset dos nós
 > `kubectl get replicaset`
 ou
  > `kubectl get rs`

> Recupera informações sobre todos os replicasets
> `kubectl describe replicaset`

> Recupera informações sobre um replicaset específico
> `kubectl describe replicaset name-replicaset`

> Cria replicaset
> `kubectl create -f replicaset-file-definition.yml`

> deleta replicaset
> `kubectl delete replicaset name-replicaset`

> escala o número de pods do replicaset
> `kubectl scale replicaset --replicas=5 name-replicaset`

