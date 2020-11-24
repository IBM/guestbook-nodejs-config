# Guestbook Nodejs Config Files

## Files 

### guestbook-configmap.yaml

This file contains the connection information for the MongoDB database that will be used in guestbook. These values are then used in the deployment object as environment variables.

### guestbook-deployment.yaml

This file contains the deployment information for the guestbook-nodejs application.

- NOTE: A kubernetes secret named `mongodb` with `username` and `password` fields is also required. Here is an example command to create the secret:

```bash
kubectl create secret generic mongodb --from-literal=username=guestbook-admin --from-literal=password=mypasswordhere

```

### guestbook-service.yaml

This file exposes the guestbook application to external traffic.