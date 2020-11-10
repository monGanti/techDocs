## Kubctl Commands

|Hint| Command|Description|
|----------|--------|-----------|
|get nodes| `kubectl get nodes` | gives information on the Nodes|
|| `kubectl cluster -info`||
|| `kubectl get nodes -o wide`|to see image details and to know which underneath OS container it is running on|
|<b><i>Running Images</i></b>|||
||`kubectl run nginx`||
||`kubectl run nginx --image=nginx`||
|<b><i>Pods</i></b>|||
|get| `kubectl get pods`|check all pods|
|| `kubectl get pods -o wide`|gives additional details of which node the pod is running on and internal ip address of the pod itself|
|create| `kubectl create -f pod-definition.yml`| kubectl create -f `<yml file name>`|
|apply| `kubectl apply -f pod-definition.yml`| alternative to create command|
|run and create| `kubectl run nginx --image=nginx`| This will create and run the pods with defined image|
|create a yml| `vi pod-definition.yml`||
|edit | `kubectl edit pod redis` | kubectl edit pod `<name of pod>` , to edit the prod conf|
|describe| `kubectl describe pod redis`| |
|describe and get specific details| `kubectl describe pod nginx | grep -i image` | directly get the details of image used|
|delete| `kubectl delete pod redis`| kubectl delete pod `<name of pod>`|


