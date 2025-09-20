### NOTES

Генериране на YAML файл:

```bash
kubectl run redis --image=redis123 --dry-run -o yaml
```

Екстрактване на информацията за Pod в YAML файл:

```bash
kubectl get pod <pod-name> -o yaml > pod-definition.yaml
```

За да модифицираш POD може да използваш и edit:

```bash
kubectl edit pod <pod-name>
```

Само долните полета са разрешени за едитване

- spec.containers[*].image
- spec.initContainers[*].image
- spec.activeDeadlineSeconds
- spec.tolerations
- spec.terminationGracePeriodSeconds
