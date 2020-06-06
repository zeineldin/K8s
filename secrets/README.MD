# Create Nginx / Apache certificate 

$ openssl genrsa -out https.key 2048
$ openssl req -new -x509 -key https.key -out https.cert -days 3650 -subj /CN=www.devopsarea.com

# Also create a dummy secret file
$ echo zein  > name

 
$ Create a kubernetes secret from this certificate and dummy file 

$kubectl create secret generic https-certificate  --from-file=https.key --from-file=https.cert --from-file=name
