# m6a-contacts-k8s
Deploying with HELM


```bash
helm repo add contacts-repo https://raw.githubusercontent.com/ozgurtaylankarakoc/m6a-contacts-k8s/main
helm install contacts-app contacts-repo/m6a-contacts-chart
```

OR

Deploying k8s yaml files with kubectl when Initially clone process has done
```bash
kubectl apply -f ./m6a-contacts-k8s/k8s/mysql-server
kubectl apply -f ./m6a-contacts-k8s/k8s/web-server
kubectl apply -f ./m6a-contacts-k8s/k8s/result-server
```
## better know details 

- ingress object will be avaible if project deployed to AWS eks service or LB reqiured enviorements
- otherwise 
- You gonna be able to see application as below.

| HTTP Method  | Action | Example|
| --- | --- | --- |
| `GET`     |   Read the records | http://[hostIP]:30001/  |
| `POST`    |   Create a new record | http://[HostIP]:30001/add  |
| `POST`    |   Update an existing record | http://[HostIP]:30001/update  |
| `POST`    |   Delete an existing record | http://[HostIP]:30001/delete  |
| `POST`    |   Delete a resource | http://[HostIP]:30002  |