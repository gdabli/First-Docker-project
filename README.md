# First-Kubernetes-Project
Simple project to learn kubernetes and its features.
### Cluter info
`kubernetes cluster-info` - provides AWS cluster information 
### Useful kubectl commands
`kubectl get nodes`- get list of all nodes along with master<br /> 
`kubectl get pods`-get list of all runnning pods<br /> 
`kubectl describe pod pod_name`- get all details about a pod<br /> 
`kubectl get deployments`- get list of running container<br /> 
`kubectl exec -it pod_name bash`- get into the container where pod is running, for troubleshooting purposes<br />
`kubectl get cm podname-config  -n namespace -o yaml` - get config details for deployment
### config
`kubectl config get-contexts`- the config file usually contains multiple clusters,users and contexts. this command will give information about which one is currently active. the user and server configuration.<br />
### Scaling of Pods using Replcation controller
`kubectl create -f file.yml`- create a replcation controller using yml file<br />
`kubectl scale --replicas=n -f replicationfile.yml`- scale up pods<br />
`kubectl delete -f file.yml`- create a replication controller<br /> 
### Deployments in kubernetes
`kubectl get deployments`- get informaton on current deployment<br />
`kubectl get rs`- get information about replica set<br />
`kubectl get pods --show-labels`- get pods, and also show labels attached to those pods<br />
`kubectl rollout status name_of_deployment`- get deployment status<br />
`kubectl set image deployment/name_of_deployment image=image:2`- run demployment with the image label version 2<br />
`kubectl edit deployment_name`- edit the deployment object<br />
`kubectl rollout status deployment_name`- get the status of rollout<br />
`kubectl rollout history deployment_name`- get the rollout history<br />
`kubectl rollout undo deployment/deployment_name`- Rollback to previous version<br />`kubectl rollout undo deployment/deployment_name --to-revision=n`- Rollback to any version
### Create admin user for kubernetes cluster to login
`kubectl create -f sample-user-filename.yml`- command to create sample user admin<br />
`kubectl -n kube-system get secret | grep admin-user`- get admin user details<br />
`kubectl -n kube-system describe secret admin-user-token-mjnb2`- get token key for admin user to login into app<br />
#### Kubernetes cluster on AWS
![](images/UI1.png)
