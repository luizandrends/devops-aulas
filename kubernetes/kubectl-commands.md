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

## kubectl delete deplo yment "deployment-name"
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