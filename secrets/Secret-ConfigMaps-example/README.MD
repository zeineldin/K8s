# In this Project we will conpine Secrets and ConfigMaps 


### Create certificate files 

`openssl genrsa -out nginx.key 2048`

`openssl req -new -x509 -key nginx.key -out nginx.cert -days 3650 -subj /CN=www.devopsarea.com`


### Create secret from this certificate 
`kubectl create secret generic nginx-certs-keys --from-file=./nginx.crt --from-file=./nginx.key`

### Create config map from nginx.conf file
`kubectl create configmap nginxconfigmap --from-file=default.conf`

### Crete Config map from index.html
`kubectl create configmap nginxindexconfigmap--from-file=index.html`

### check using
`curl -kI https://<IP>:<PORT>`
