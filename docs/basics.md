# Basics

## kubectl

For more details see [kubectl quick reference](https://kubernetes.io/docs/reference/kubectl/quick-reference/)

Global options:

* ```-n <namespace>``` Sets the namespace for the command. If not set, defaults to the 'default' namespace

### List resources

```kubectl get <resource> -o <option> -n <namespace>```

Where:
* ```<resource>``` is the type of resource to get. I.e. pods, services, deployments, pvs
* ```-o <option>``` Optional. Changes the output. Couple of examples:
  * wide - shows more details
  * yaml - outputs in yaml format, same as the manifests

### Get Resource

```kubectl get <resource> <name> -o <option> -n <namespace>```

Same as list resource, except:
* ```<name>``` name of the resource to get

### Show logs

```kubectl logs <pod> -n <namespace> -f```

Where:
* ```<pod>``` name of the pod to show logs for
* ```-f``` Optional. Continues to tail the output

### Connect to Pod

```kubectl exec --stdin --tty <pod> -n <namespace> -- /bin/sh```

Where:
* ```<pod>``` name of the pod to connect to

### Copy file to/from pod

*Copy to the pod*
```kubectl cp <local dir> <namespace>/<pod>:<pod dir>```

*Copy from the pod*
```kubectl cp <namespace>/<pod>:<pod dir> <local dir>```

### Get pod resource usage

```kubectl top pod <pod> -n <namespace>```

