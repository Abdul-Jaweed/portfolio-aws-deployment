# Portfolio AWS Deployment

**Description: About the Deployment**

```
1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2
```
## 1. Login to AWS Console.

## 2. Create IAM (Identity and Access Management) User for Deployment


**with specific access**
```
1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws
```

**Policy**

```
1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```

## 3. Create ECR repo to store/save docker image

```
- Save the URI: url/appname
```

## 4. Create EC2 Machine (Ubuntu)


## 5. Open EC2 and Install Docker in EC2 Machine:

**Optional**

```bash
sudo apt-get update -y

sudo apt-get upgrade -y
```

**required**

```bash
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

## 6. Configure EC2 as self-hosted runner:

```
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```

## 7. Setup github secrets:

```
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = ap-south-1

AWS_ECR_LOGIN_URI = demo>> appuri-south-1.amazonaws.com

ECR_REPOSITORY_NAME = appname
```