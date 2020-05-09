# To access the 1st container 

```kubectl exec -it <pod_name /bin/bash>```

OR 

```kubectl exec -it mc1 -c 1st <pod_name /bin/bash>```

# To access the 2nd container 

```#kubectl exec -it mc1 -c 2nd /bin/bash```
