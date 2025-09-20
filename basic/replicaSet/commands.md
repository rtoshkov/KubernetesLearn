### Notes

#### Scale

---

update yaml file for replocaset

```bash
kubectl replace -f replicaset-definition.yml
```

! Долните два варианта няма да ъпдейтнат файла и ще имаш различна информация във файла и на средата

```bash
# Method 1
kubectl sclae --replicas=6 -f replicaset-definition.yml
# Method 2
kubectl scale --replicas=6 replicaset <replicaset-name>
```
