# RabbitMQ on EKS Cluster #

**Create a Namespace** 
`kubectl create ns rabbits`

**Check Storage Class**
`kubectl get storageclass`

**Deploy the required files**
`kubectl apply -n rabbits -f rabbit-rbac.yaml`

`kubectl apply -n rabbits -f rabbit-configmap.yaml`

`kubectl apply -n rabbits -f rabbit-secret.yaml`

`kubectl apply -n rabbits -f rabbit-statefulset.yaml`

**Port Fowarding**

`kubectl -n rabbits port-forward rabbitmq-0 8080:15672`

**CleanUP**
`kubectl delete -n rabbits -f abc.yaml`

`kubectl delete pvc --all` 