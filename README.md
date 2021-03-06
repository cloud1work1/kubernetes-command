# kubernetes-command
## Kubernetes Deployment
- kubectl create deployment &lt;Deployment-name&gt; --image=&lt;imagename:tag&gt;
- kubectl get deployments
- kubectl get deploy
- kubectl describe deployment &lt;deployment-name&gt;
- kubectl get replicasets
- kubectl get rs
- kubectl get pods
- kubectl scale --replicas=&lt;number&gt; deployment &lt;deployment-name&gt;
- kubectl expose deployment &lt;Deployment--name&gt; --type=NodePort --port=&lt;port-no&gt; --target-port=&lt;target-poert-no&gt; --name=&lt;Service-name&gt;
- kubectl get svc
- kubectl get nodes
- kubectl get nodes -o wide  

## Kubernetes Deployment modification
 - kubectl get deployment &lt;deployment-name&gt; -o yml
 - kubectl set image deployment/&lt;deployment-name&gt; &lt;container-name&gt;=&lt;container-image&gt; --record=true
 - kubectl rollout status deployment/&lt;deployment-name&gt;
 - kubectl rollout history deployment/&lt;deployment-name&gt; 
 - kubectl rollout undo deployment/&lt;deployment-name&gt;
 - kubectl rollout undo deployment/&lt;deployment-name&gt; --to-revision=&lt;revision-number&gt;
 - kubetcl rollout restart deployment/&lt;deployment-name&gt;
 - kubectl rollout pause deployment &lt;deployment-name&gt;
 - kubectl set resources deployment/&lt;deployment-name&gt; -c=kubeginx --limits=cpu=200m,memory=512mi
 - kubectl rollout resume deployment/&lt;deployment-name&gt;
 - kubectl delete deployment &lt;deployment-name&gt;
 - kubectl delete svc &lt;service-name&gt;
 
## Kubernetes Edit Deployment using edit command
-  kubectl edit deployment/&lt;Deployment-Name&gt; --record=true =&gt; change spec.containers.image (yml format)

## Kubernetes create and work with pods
- kubectl run &lt;pod-name&gt; --image &lt;image-name&gt; --generator=run-pod/v1
- kubectl run &lt;pod-name&gt; --image &lt:image-name&gt;
- kubectl describe pod &lt;pod-name&gt;
- kubectl delete pod &lt;pod-name&gt;
- kubectl expose pod &lt;pod-name&gt; --type=NodePort --port=&lt;Port-Number&gt; --name=&lt;Service-Name&gt;
- kubectl expose pod &lt;pod-name&gt; --type=NodePort --port=&lt;Port-Number&gt; --target-port=&lt;exposed-port-number&gt; --name=&lt;Service-name&gt;

- kubectl config view --minify
- kubectl logs &lt;pod-name&gt;
- kubectl logs -f &lt;pod-name&gt;
- kubectl exec -it &lt;pod-name&gt; -- /bin/sh
- kubectl exec -it &lt;pod-name&gt; &lt;command-to-execute&gt;
- kubectl get pod &lt;pod-name&gt; -o yaml
- kubetcl get svc &lt;service-name&gt; -o yaml
- kubectl get all
- kubectl delete pod &lt;pod-name&gt;
- kubectl delete svd &ltservice-name&gt;




## EKS Cluster
- eksctl create cluster --name=&lt;node-name&gt; --region=&lt;region-name&gt; --zones=&lt;zone-name-comma-separated&gt; --without=nodegroup
- eksctl get clusters
- eksctl utils associate-iam-oidc-provider --region &lt;region-name&gt; --cluster &lt;cluster-name&gt; --approve
- eksctl create nodegroup
- eksctl get nodegroup --cluster=&ltcluster-name&gt;


