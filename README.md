# kubernetes-command
## Kubernetes Deployment
- kubectl create deployment <Deployment-name> --image=<imagename:tag>
- kubectl get deployments
- kubectl get deploy
- kubectl describe deployment <deployment-name>
- kubectl get replicasets
- kubectl get rs
- kubectl get pods
- kubectl scale --replicas=<number> deployment <deployment-name>
- kubectl expose deployment <Deployment--name> --type=NodePort --port=<port-no> --target-port=<target-poert-no> --name=<Service-name>
- kubectl get svc
- kubectl get nodes
- kubectl get nodes -o wide  
