# MAIN

### Links

- [LearnKodeKloud](https://learn.kodekloud.com/user/dashboard)  
- [Coursera: Deploy containers by using Azure Kubernetes Service free](https://www.coursera.org/learn/deploy-containers-with-azure-kubernetes-service?campaignid=20858198824&adgroupid=&device=c&keyword=&matchtype=&network=x&devicemodel=&creativeid=&assetgroupid=6490027433&targetid=&extensionid=&placement=&gad_campaignid=20854471652)

---

- kubectl get replicationcontroller
```bash
NAME       DESIRED   CURRENT   READY   AGE
myapp-rc   3         3         3       93s
```

- kubectl get replicaset
```bash
NAME               DESIRED   CURRENT   READY   AGE
myapp-replicaset   3         3         3       11s
```
  
  
---
- kubectl get all
```bash
NAME                                    READY   STATUS    RESTARTS   AGE
pod/myapp-deployment-56db76d944-jqj59   1/1     Running   0          77s
pod/myapp-deployment-56db76d944-lptk9   1/1     Running   0          77s
pod/myapp-deployment-56db76d944-r42pq   1/1     Running   0          77s

NAME                 TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)   AGE
service/kubernetes   ClusterIP   10.96.0.1    <none>        443/TCP   31h

NAME                               READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/myapp-deployment   3/3     3            3           77s

NAME                                          DESIRED   CURRENT   READY   AGE
replicaset.apps/myapp-deployment-56db76d944   3         3         3       77s
```

#### Notes:
> 30KK to get 30% OFF 


