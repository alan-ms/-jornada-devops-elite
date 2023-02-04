# Jornada DevOps de Elite

### Kubernetes
Foi criado o `./k8s/deployment.yml` para deploy da aplicação em um cluster do Kubernetes. Foi utilizado as ferramentas [`k3d`](https://k3d.io/v5.4.6/) e [`kubectl`](https://kubernetes.io/docs/tasks/tools/) para utilização do Kubernetes localmente.

## Comandos Kubernetes (k3d - kubectl)
  - `k3d cluster create --nome_cluster--` | Criação de cluster
  - `k3d cluster create --nome_cluster-- --no-lb` | Criação de cluster sem LoadBalancer
  - `k3d cluster create --nome_cluster-- -p "80:30000@loadbalancer"` | Criação de cluster colocando a porta 80 apontando para porta 30000 do loadbalancer, colocando assim uam entrada única para os pods do cluster
  - `k3d cluster delete --nome_cluster--` | Exclusão de cluster pelo nome
  - `kubectl get pod` | Listar pods do cluster
  - `kubectl describe pod|service|deployment` | Descrever pod do cluster
  - `kubectl cluster-info` | Informações sobre o cluster
  - `kubectl api-resource` | Exibe os recursos suportados pela API
  - `kubect apply -f deployment.yml` | Criar ou realizar o update de configuração de pods, replicasets, services e deployments do cluster
