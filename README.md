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
 
## Kubernetes Edit Deployment using edit command
-  kubectl edit deployment/&lt;Deployment-Name&gt; --record=true =&gt; change spec.containers.image (yml format)

## Kubernetes create and work with pods
- kubectl run &lt;pod-name&gt; --image &lt;image-name&gt; --generator=run-pod/v1
- kubectl run &lt;pod-name&gt; --image &lt:image-name&gt;
- kubectl describe pod &lt;pod-name&gt;
- kubectl delete pod &lt;pod-name&gt;
