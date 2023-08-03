# Boilerplate Code

## Kubernetes 

Deployment.yml


## Private Repo Docker Registery

### AWS ECR EXAMPLE 
Before you Run this you must set up the AWS CLI on the host first. 
```
kubectl create secret docker-registry regcred \
  --docker-server=${AWS_ACCOUNT}.dkr.ecr.${AWS_REGION}.amazonaws.com \
  --docker-username=AWS \
  --docker-password=$(aws ecr get-login-password) \
  --namespace=health-check
```