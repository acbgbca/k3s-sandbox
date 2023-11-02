# Portainer

From https://docs.portainer.io/start/install-ce/server/kubernetes/baremetal

## kubectl

To install Portainer using kubectl, run the following command:
```
kubectl apply -n portainer -f https://downloads.portainer.io/ce2-19/portainer.yaml
```

Note that doesn't include an Ingress. To setup an ingress at 'portainer.local' run:
```
kubectl apply -n portainer -f ./manifests/portainer-ingress.yaml
```

* Go to http://localhost:3000 and navigate to 'http://portainer.local' in the embedded browser.
* Setup a username and password
* Select 'Get Started'

You should now have access to the cluster

## helm