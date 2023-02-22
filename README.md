# Conceitos de AKS.

**O que é um AKS?**

 Azure Kubernets Service é um Cluster, o mesmo criar Container que é uma virtualização do embiente que executará uma ou diversas aplicações das mais diferentes stacks, porém possui seus próprios comandos internos. Como por exemplo o Kubectl.

 O AKS é muito utilizado para gerenciamento de Microserviços.

**Quando usar o AKS:**

- Gestão complexo, Envolvemento **Microsserviços**
- Equipe qualificada (Pessoas que possuem conhecimento na ferramenta)
- Picos de utilização e/ou altas cargas de processamento.

 **Quando NÃO usar:**

- Gestão fácil
- Pouca Escola
- Cenário Simples

## Kubectl - Comands

- *Para deletar um YAML:*
    
    `kubectl delete -f name.yml`
    
- *Deletar tudo que está dentro do NAMESPACE:*
    
    `kubectl delete all --all -n NOME_DO_NAMESPACE`
    
- *Editar o arquivo coredns:*
    
    `kubectl edit cm coredns -n kube-system`
    
- *Visualizar todos os pods e o status:*
    
    `kubectl get pods -n kube-system`
    
- *visualizar o dns no aks:*
    
    `kubectl get services -n kube-system`
    
- *visualizar a descrição do dns:*
    
    `kubectl describe service kube-dns -n kube-system`
    
- *Aplicar custom-dns:*
    
    `kubectl apply -f corednsms.yaml`
    
- *verificar se o custom-dns subiu no Configmap:*
    
    `kubectl get configmaps --namespace=kube-system coredns-custom -o yaml`
    
- *Restart pods DNS:*
    
    `kubectl rollout restart deploy--namespace kube-system -l k8s-app=kube-dns`
    
- *Verificar o SSD/HD:*
    
    `kubectl get persistentvolume`
    
    `kubectl get persistentvolume <pvc-e10a5b99-1c21-4cf7-b6c8-6025e22001d3> --output yaml`
    
- *verificar qual os serviços que estão rodando:*
    
    `kubectl get services`
    
- *Mudar para um NameSpace diferente no AKS:*
    
    `kubectl config set-context —current —namepasce=<nome_do_namespace`>
    
- *Verificar pods de qualquer namespace sem precisar acessa-lo:*
    
    `kubectl get pods —namespace=<nome_do_namespace>`
    
- Verifficar utilização de CPU e memoria dos pods/nods:
    
    `kubectl top pods - nodes`
    

## **Criando um AKS na prática e configurando.**

**Em Construção**
