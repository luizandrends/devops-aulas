Helm commands

## helm install <name> <package-name>

CLI para a criação de um pacote helm

## helm repo list

CLI para a listagem de repositorios

## helm fetch <package-name>

CLI para fazer download de um pacote localmente

## helm repo <file-name> <path>

CLI para criar um index dos pacotes instalados

## helm repo add <url>

CLI para adicionar um repositorio na instalacao do helm provicenciando a URL do repositorio

## helm repo list

CLI para lista os repositorios. Mostra somente os repositorios cacheados localmente

## helm repo update .

CLI para fazer o update dos repositorios locais

## helm repo remove <repo-name>

CLI para remover os repositorios do helm providenciando a URL

##  helm install <repo-name> <path> --dry-run 

CLI para gerar o manifesto helm

## helm show values <path>

CLI para mostrar o values.yaml do chart

## helm install <chart-name> <path> --set image.<image-name> --dry-run

CLI para sobrescrever a imagem do values

  A flag --set serve para fazer um stack de modificações.

  helm install demo ./example --set image.tag=latest --set service.type=NodePort --dry-run

## helm install <chart-name> <path> -f <file-path> --dry-run

CLI para sobrescrever o chart baseado em um arquivo

