# In this Project we will conpine Secrets and ConfigMaps 


### Create certificate files 
`openssl req -newkey rsa:2048 -nodes -keyout nginx.key -x509 -days 365 -out nginx.crt`

### Create secret from this certificate 
`kubectl create secret generic nginx-certs-keys --from-file=./nginx.crt --from-file=./nginx.key`

### Create config map from nginx.conf file
`kubectl create configmap nginxconfigmap --from-file=default.conf`

### Crete Config map from index.html
`kubectl create configmap nginxindexconfigmap--from-file=index.html`

### check using
`curl -kI https://<IP>:<PORT>`
