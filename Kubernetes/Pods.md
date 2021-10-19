# Pods 

## Conceitos
* O `k8s` não implanta containers diretamente no nós `worker`. Os containers são encapsulados em objeto interno, conhecido como `Pod`;
* É uma instância de uma aplicação
* É o menor objeto que se pode criar no k8s;
* Para escalar uma aplicação para aguentar uma maior quantidade de trafego, aumenta-se o número de `Pods` e não de containers em um `Pod`
* Caso o [[Arquitetura#Nó nodes | nó]], não tenha recursos necessários para rodar mais que uma instância da aplicação, é possível subir o `pod` em um novo [[Arquitetura#Nó nodes | nó]].

## Multi-container pods
* Geralmente um `pod` possui uma relação `1:1` com containers rodando a aplicação. Para `scale up` você adiciona um pod, para `scale down` remove-se o pod.
* Um `pod` pode conter mais que um container, geralmente com tarefas de suporte ao container principal da aplicação; Os containers dentro do `pod` escalarão juntos.
* Pode-se referenciar os containers por `localhost` para comunicação, já que compartilham o mesmo namespace de rede. Assim como o namespace de storage (IPS?) 

## Pod Definition
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: myapp
  labels:
    application: myapp
    tier: frontend
spec:
  containers:
  	- name: nginx
	  image: nginx:latest
	- name: redis
	  image: redis:latest

```

## Comandos úteis
> Encapsula uma docker image em um Pod e a executa no cluster
> `kubectl run nginx --image nginx`

> Recupera a lista de todos os Pods
> `kubectl get pods`

> Edita um pod a partir de sua definição
>  `kubectl edit pod podname`

> Aplica(cria ou atualiza) uma [[ApiObjects | definição de um objeto]] no cluster
> `kubectl apply -f pod-definition.yaml`
 
 > Cria uma [[ ApiObjects | definição de um objeto]] no cluster
> `kubectl create -f pod-definition.yaml`
 
 
> Descreve todas as informações de todos os pods em um determinado namespaces (padrão: default)
> `kubectl describe pod`

> Descreve todas as informações de um pod em um determinado namespaces (padrão: default)
>  `kubectl describe pod/pod-name`

> Recupara todos os pods de todos os namespaces e imprime mais informações
> `kubectl get pods --all-namespaces -o wide`

> Recupara todos os pods com a informação das labels
> `kubectl get pods --show-labels`

> Recupera todos os pods que estão estão rodando
> `kubectl get pods --field-selector status.phase==Running`

> Recupera todos os pods que estão estão rodando no namespace default
> `kubectl get pods --field-selector status.phase==Running,metadata.namespace=default`