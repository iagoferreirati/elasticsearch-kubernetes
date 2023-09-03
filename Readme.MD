# Configuração do Elasticsearch, Kibana e APM no Kubernetes

Este guia descreve como configurar o Elasticsearch, Kibana e APM no Kubernetes usando o Elasticsearch Operator (ECK).

## Passo 1: Adicionar o repositório Helm do Elastic

```bash
helm repo add elastic https://helm.elastic.co
helm repo update
```

## Passo 2: Passo 2: Instalar o Elastic Operator
```bash
helm install elastic-operator elastic/eck-operator -n elastic-system --create-namespace
```

## Passo 3: Criar um cluster Elasticsearch
```bash
kubectl apply -f elasticsearch.yaml
```

## Passo 4: Instalar o Kibana
```bash
kubectl apply -f kibana.yaml
```

## Passo 5: Instalar o APM
```bash
kubectl apply -f apm.yaml
```