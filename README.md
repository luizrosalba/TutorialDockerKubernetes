Tutorial Docker e Kubernetes
============================

Este repositório é um tutorial sobre Docker e Kubernetes, ele traz os principais comandos utilizados e alguns conceitos na apresentação. Ele foi criado para o Bootcamp que a Avanade criou para formação de Devs, e pode ser utilizado ou copiado livremente. Apenas peço que dê o crédito se for copiar.

Este tutorial foi pensado para profissionais de desenvolvimento de sitemas, que querem conhecer Docker e Kubernetes, então temas como instalação e operação não são cobertos.

Os slides que eu uso para passar os conceitos principais sobre Docker e Kubernetes estão disponíveis [aqui](Tutorial-Docker-Kubernetes.pdf).


# Orquestração de serviços em plataformas escaláveis com docker e kubernets 

### Docker 

Imagens -> docker run -> running containers

- containers são mb de ordem de grandeza 
- consomem menos recursos 

d roda em background 
o nome da imagem está no dockerhub 

- docker run -d -p  3000:80 docker/getting-started

- usar windows 10 com subsystem for linux para desempenho 

- docker ps  (lista)
 
- docker stop id (para)

- docker ps -a lista todos inclusive os que nao estao rodando 

- docker rm ad (mata o docker)

- docker build --tag meu-container:1.0 .   (faz o build com os parametros que voce forneceu )

- docker image list lista as imagens 


23 22 

Pré-Requisitos
--------------

Para rodar estes exemplos, é necessário:

1. Ter uma conta no Azure, com créditos disponíveis (a opção de [trial](https://azure.microsoft.com/pt-br/free/) gratuito funciona!)
2. Ter o [Azure Cli](https://docs.microsoft.com/pt-br/cli/azure/install-azure-cli?view=azure-cli-latest) instalado
3. Estar com o Azure cli logado na conta que deve ser utilizado e utilizando a subscription correta
4. Ter o [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) instalado
5. Ter o [Docker Desktop](https://www.docker.com/products/docker-desktop) instalado, e configurado.
6. Garantir que seu Docker está configurado para rodar [Containers Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
7. [Criar um cluster AKS e registro ACR](ambiente/1-Criando-um-cluster-AKS/README.md)


Tutoriais sobre Docker
------------------

1. [Rodando um Container Localmente](docker/1-Rodando-um-Container-localmente/README.md)
2. [Dockerfile simples](docker/2-Dockerfile-simples/README.md)
3. [Dockerfile multi-stage](docker/3-Dockerfile-multi-stage/README.md)
4. [Publicando uma imagem no ACR](docker/4-Publicando-imagem-acr/README.md)

Tutoriais sobre Kubernetes
----------------------

1. [Criando um namespace](kubernetes/1-Criando-um-Namespace/README.md)
2. [Rodando uma Pod](kubernetes/2-Rodando-uma-Pod/README.md)
3. [Rodando um deployment com mais de uma Pod](kubernetes/3-Rodando-um-Deployment/README.md)
4. [Rodando um service](kubernetes/4-Rodando-um-Service/README.md)
5. [Escalando horizontalmente um deployment](kubernetes/5-Escalando-horizontalmente-um-deployment/README.md)
6. [Publicando nossa aplicação](kubernetes/6-Publicando-nossa-aplicacao/README.md)

Desenvolvimento Futuro
----------------------

Lista de tópicos que eu pretendo adicionar a este tutorial, e que podem ser úteis para quem quiser aprofundar os estudos:

- Como utilizar quotas para restringir um namespace
- Explicação detalhada sobre Deployment e ReplicaSet
- Probes (readiness, liveness)
- Utilização de Ingress
- Utilização de Services para mapear serviços externos
- Utilização de Persistent Volume e Persistent Volume Claims
- Utilização de StatefulSet para criar serviços persistentes
- Utilização de Secrets
- Segurança: Network Policy
- Segurança: Controle de Acesso
- Pods com mais de um container (Sidecar, etc...)
- Ferramentas de template (Helm / Kustomize)
- Uso de Jobs
- Uso de Init Containers
- Uso do KEDA para escalar por filas
- Uso de Node Pools
- Uso de Node Affinity e Node Anti-affinity para controlar onde roda um serviço
- Container Windows e Linux rodando no mesmo cluster
- Monitoramento do AKS com App Insights

Agradecimentos
--------------

Gostaria de agradece ao stefanprodan, que publicou a excelente imagem docker [podinfo](https://github.com/stefanprodan/podinfo) que foram utilizadas em alguns demos.
