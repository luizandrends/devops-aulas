### KUBECTL COMMANDS

## kubectl create "name" --image=image-name

CLI para criar um pod (Deployment=abstração para pods do K8s)

## kubectl get pods

CLI para listar todos os pods

## kubectl get pods -o wide

CLI para listar os pods mais detalhadamente

## kubectl get replicaset

CLI para listar

## kubectl describe pods

CLI para mostrar os manifestos e eventos dos pods

## kubectl describe nodes

CLI para mostrar os manifestos e eventos dos nodes

## kubectl edit deployment "deployment-name"

CLI para editar o manifesto do deployment

## kubectl logs "pod-name"

CLI para pegar os logs do pod

## kubectl exec -it "pod-name" -- bin/bash

CLI para entrar no bash do pod

## kubectl delete deployment "deployment-name"

CLI para excluir um pod em específico

## kubectl apply -f "file name"

CLI para criar deployments por arquivos. Tambem podemos editar
os deployments por este comando sem a necessidade de excluir deployments. O estado do deployment vem do ETCD.

## kubectl get services

CLI para listar todos os services

## kubectl describe service "service name"

CLI para mostrar os dados de um service

## get deployment "deployment name" -o yaml

CLI para mostrar o estado do deployment

## kubectl delete -f "file name"

CLI para remover pods e serviços por arquivo

## kubectl get all

CLI para listar todos os componentes rodandos
(Muito util com | grep "palavra chave")

## kubectl get namespaces

CLI para a listagem das namespaces

## kubectl cluster-info

CLI para mostrar as infos gerais do cluster

## kubectl create namespace "namespcace name"

CLI para a criação de namespaces

## kubectl apply -f "file name" --namespace="namespace name"

CLI para a criação de componentes dentro de uma namespace específica

    Podemos tambem utilizar sem a flag --namespace declarando dentro do
    metadata um campo chamado namespace com o nome da mesma.

## kubectl get pods -n "namespace name"

CLI para a listagem de pods dentro de uma namespace em específico

## kubectl get deployments -n "namespace name"

CLI para a listagem de deployments dentro de uma namespace em específico

## kubectl get hpa -n "namespace name"

CLI para mostrar o HPA do cluster

## Instalação kubens

brew install kubens

## kubens

CLI para mostrar todas as namespaces e a namespace ativa

## kubens "namespace name"

CLI para alterar a namespace ativa

## kubectl drain "node-name"

CLI para "paralizar" o node parametrizado

<strong>"Drain":</strong> O comando drain "Paraliza" o node parametrizado e transfere os pods do deployment para outros pods com espacos disponiveis.

<strong>"DaemonSet System Pods":</strong> Sao pods criados pelo sistema do K8S ou seja, quando executamos o comando com a flag --ignore-daemonsets --force estamos deletando permanentemente os DaemonSet System Pods, por isso precisamos ter muita cautela e conhecimento do ambiente antes de executar esse comando

## kubectl uncordon "node-name"

CLI para voltar o node parametrizado ao uso

    Este comando nao voltara os pods antigos ao seu lugar.

## kubectl get ingresses

CLI para listar todos os ingress do cluster

## kubectl get pods -n namespace --selector k8s-app=label

CLI para pegar os pods em uma namespace filtrando pela label

## kubectl exec pod-name -c containerName -- comando

CLI para executar acoes dentro de um container de um pod

## kubectl get pv

CLI para pegar os volumes persistentes do cluster

## kubectl create deployment my-deployment --image=imageName

CLI para criar deployment sem um arquivo yaml

## kubectl get sa

CLI para a listagem dos service account

## kubectl get sa -n "namespace"

CLI para a listagem dos service account em uma namespace

## kubectl create sa -n "namespace"

CLI para a criacao de um service account

    Os service accounts diferente das roles funcionam como "permissoes" para os pods

## kubectl top pod -n namespace --sort-by JSONPATH --selector app=POD LABEL

CLI para mostrar as metricas de uso de um pod

## kubectl "COMMAND" --dry-run=client

CLI que faz um "plan"

## kubectl label nodes <node name> special=true

Cli para colocar label no node desejado

## kubectl edit "component type" "component name"

Cli para abrir um editor e editar o componente desejado

## kubectl scale deployment.v1.apps/"deployment-name" --replicas="desired replicas"

Cli para fazer scale (down ou up) em um deployment

## kubectl rollout status deployment.v1.apps/"deployment-name"

Cli para fazer o rollout da ultima alteração feita

## kubectl set image deployment/deployment-name deployment-name=image:version

Cli para trocar uma imagem de um deployment

## kubectl rollout history deployment.v1.apps/my-deployment

Cli para ver as revisions de um deployment

## kubectl get endpoints "service-name"
CLI para listar os endpoints de um servico

Caso seja um deployment com multiplos pods, o comando ira retornar uma lista nesse formato: 192.168.126.51:80,192.168.126.52:80,192.168.194.125:80 
