# Service
* Service é utilizado para expor um aplicativo em execução em um conjunto de pods como um serviço de rede. Desta forma permite realizar o bind da porta do cpod com a porta do nó K8S.

* Existem 3 tipos de services:
- NodePort:
- ClusterIP:
- Load Balancer:

## Comandos úteis
 
 > Cria service
> `kubectl create -f service-file-definition.yml`

 > Recupera informações sobre o service
 > `kubectl get svc`

> Deleta service
> `kubectl delete svc name-service`

