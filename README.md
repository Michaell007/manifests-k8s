
# Kustomize

A brief description kustomize

## Running Tests

Tester le rendu Kustomize avant de déployer
```bash
kubectl kustomize overlays/production
```

Si tu veux vérifier les changements avant d'appliquer
```bash
kubectl diff -k overlays/production
```

Appliquer au cluster
```bash
kubectl apply -k overlays/production
```

Supprime proprement tous les objets gérés par ce kustomization
```bash
kubectl delete -k overlays/production
```

Forcer un redéploiement des pods
```bash
kubectl rollout restart deployment backend -n production
kubectl rollout restart deployment frontend -n production
```
