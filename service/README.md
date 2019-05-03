# Regarding  nginx-service-ClusterIP-5.yml

### check the pods

```kubectl get pods```

### login to the pod

```kubectl exec -it [YOUR_POD_NAME] -- sh```

### install curl 

```apk add --no-cache curl```

### see the index.html output 
```curl [CLUSTER_IP]:80 ```
