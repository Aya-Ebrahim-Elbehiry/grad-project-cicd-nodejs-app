# Graduation-Project-ITI

## ssh vm instance

```bash
gcloud compute ssh private-vm --project iti-1-366311 --zone us-central1-a -- -L8888:127.0.0.1:8888
```

## Install kubctl


## then connect to the cluster (GKE)

```bash
gcloud container clusters get-credentials gke-cluster --zone us-central1-a --project iti-1-366311
```

### Install docker



### Install git



### Install gcloud



### Install open-jdk

To connect the slave in jenkins with cloud vm-instance 



### Build docker image for Jenkins


### Create namespace then deploy Jenkins

```bash
kubectl create namespace jenkins-ns
kubectl config set-context --current –namespace=jenkins-ns
kubectl create -f app-deployment.yaml
kubectl create -f app-service.yaml
```


**Jenkins link : [http://35.202.111.14:8080](http://35.202.111.14:8080/)**









-username of instance to ssh



Here the credentials created



## Let’s create slave



## Build pipeline that pull docker file from git then build the image of the application then push it to dockerhub then deploy the application



Image pushed successfully

**Pipline automated successfully**

## Get IP:Port for the application


## OR


# Finalyyy

## App link: [http://34.68.90.32:3000/](http://34.68.90.32:3000/)
