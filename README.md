Simple K8s Examples 

# apply the deployment 
```kubectl run  webserver --image=nginx  --port= 80 -- replicas=2```

# Expose the deployment into service
```kubectl expose deployment webserver  --name web-service  --type=LoadBalancer --port=80```

# scale the pods 
```kubectl scale --replicas=4 deployment/webserver```

# check all pods 
```kubectl get pods```

# check all services 
```kubectl get service```

# delete pods 
```kubectl delete pod  <pod_name> ```

# check service URL
```minikube service <service_name> --url```

# delete servie 
```kubectl delete services <service_name>``` 

# delete pods 
```kubectl delete pos <pod_name>```

# delete all pods 
```kubectl delete pods --all```

# login to the pods
``` kubectl exec -it <pos_name>  -- /bin/bash```


-------------------------------

#apply deployment from a file 
```kubectl apply -f <deployment_file>

#apply service from a file
```kubectl apply -f <service_file>
