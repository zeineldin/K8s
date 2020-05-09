# To access the 1st container 

```kubectl exec -it <pod_name /bin/bash>```

OR 

```kubectl exec -it mc1 -c 1st /bin/bash>```

# To access the 2nd container 

```#kubectl exec -it mc1 -c 2nd /bin/bash```


# check logs 

```kubectl logs -f mc1 -c <container_name>```
