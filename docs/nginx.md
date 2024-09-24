# Nginx

To install Nginx run the following command:
```
kubectl apply -n nginx -f ./manifests/nginx.yaml
```

Nginx can then be accessed using the packaged browser at 'http://localhost:3000', by navigating to 'http://nginx.local'

## With persistent volume

```
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: nginx-pvc
  namespace: nginx
spec:
  accessModes:
    - ReadWriteOnce
  storageClassName: local-path
  resources:
    requests:
      storage: 2Gi
```