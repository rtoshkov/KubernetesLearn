- kubectl run nginx --image nginx  
- kubectl get pods  
```bach
NAME    READY   STATUS    RESTARTS   AGE
nginx   1/1     Running   0          4m4s
```

---

- kubectl describe pod nginx

```bash
Name:             nginx
Namespace:        default
Priority:         0
Service Account:  default
Node:             docker-desktop/192.168.65.3
Start Time:       Tue, 09 Sep 2025 18:19:23 +0300
Labels:           run=nginx
Annotations:      <none>
Status:           Running
IP:               10.1.0.6
IPs:
  IP:  10.1.0.6
Containers:
  nginx:
    Container ID:   docker://c88539f22f1ad4d87e871035dd903cec8c782f0f8af4b1051de84a349ee0d04f
    Image:          nginx
    Image ID:       docker-pullable://nginx@sha256:d5f28ef21aabddd098f3dbc21fe5b7a7d7a184720bc07da0b6c9b9820e97f25e
    Port:           <none>
    Host Port:      <none>
    State:          Running
      Started:      Tue, 09 Sep 2025 18:19:58 +0300
    Ready:          True
    Restart Count:  0
    Environment:    <none>
    Mounts:
      /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-4vnqd (ro)
Conditions:
  Type                        Status
  PodReadyToStartContainers   True
  Initialized                 True
  Ready                       True
  ContainersReady             True
  PodScheduled                True
Volumes:
  kube-api-access-4vnqd:
    Type:                    Projected (a volume that contains injected data from multiple sources)
    TokenExpirationSeconds:  3607
    ConfigMapName:           kube-root-ca.crt
    ConfigMapOptional:       <nil>
    DownwardAPI:             true
QoS Class:                   BestEffort
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
Events:
  Type    Reason     Age    From               Message
  ----    ------     ----   ----               -------
  Normal  Scheduled  5m3s   default-scheduler  Successfully assigned default/nginx to docker-desktop
  Normal  Pulling    5m1s   kubelet            Pulling image "nginx"
  Normal  Pulled     4m31s  kubelet            Successfully pulled image "nginx" in 30.68s (30.68s including waiting). Image size: 192385289 bytes.
  Normal  Created    4m28s  kubelet            Created container: nginx
  Normal  Started    4m28s  kubelet            Started container nginx
```

---

- kubectl get pods -o wide
```bash
NAME    READY   STATUS    RESTARTS   AGE     IP         NODE             NOMINATED NODE   READINESS GATES
nginx   1/1     Running   0          7m15s   10.1.0.6   docker-desktop   <none>           <none>
```

---

