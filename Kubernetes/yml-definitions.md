## pod-definition.yml 

apiVersion: v1
kind: Pod
metadata:
 name: my-app
 labels:
   app: myapp
   type: front-end

spec:
  containers:
   - name: nginx-container
     image: nginx

## Kinds and Versions
|Kinds|Version|
|POD|v1|
|Service|v1|
|ReplicaSet|apps/v1|
|Deployment|apps/v1|