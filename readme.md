# Setup

1. Install Helm and Helmfile, may require the plugin helm-diff
1. Setup AWS Credentials to allow pulling from ECR images (https://github.com/nabsul/k8s-ecr-login-renew)
```
kubectl create generic ecr-renew-cred \
  --from-literal=REGION=[AWS_REGION] \
  --from-literal=ID=[AWS_KEY_ID] \
  --from-literal=SECRET=[AWS_SECRET]
```
1. Apply all YAML files