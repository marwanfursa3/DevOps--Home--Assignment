# DevOps--Home--Assignment

Dev-Ops Home Assignment

1. Create a local k8s cluster based on the following tutorial:  [MongoDB and Express.js REST API tutorial](https://www.mongodb.com/languages/express-mongodb-rest-api-tutorial).
    1. Clone the git repo into your local machine.
    2. Create Dockerfile for the app and server directories
       Note: make sure you choose the right base image for each.
    3. Create a k8s cluster based on the provided topology (see the
       image below) with a MongoDB container instead of the Atlas
       instance that was mentioned in the tutorial.
2. Create a k8s Job/App (written in your preferred Coding/Scripting
language) containing the following steps:
    1. Import the provided (Link for Dump) MongoDB Dump into the
       MongoDB instance in the k8s cluster.
    2. Communicate with the API and do the following:
       • Create a new post.
       • List all the available posts and Save the results into CSV file.


## make sure that you have
- **Docker**: For containerization of the application and server.
- **Kubernetes**: For orchestration of the containers (Minikube or Kind recommended).
- **Git**: For cloning the repository.


## Setup
### 1. Clone the Git Repository 
```
git clone https://github.com/marwanfursa3/DevOps--Home--Assignment.git
```

## How To Run

Clone the git repo into your local machine.

![alt text](https://github.com/marwanfursa3/DevOps--Home--Assignment/blob/main/Screenshot%202024-09-24%20at%201.26.34.png)



1. Start the Express server:
```
cd server
kubectl apply -f express-server-deployment.yaml
```

2. Start the React app :
```
cd app
kubectl apply -f app-deployment.yaml

Open https://localhost:3000 on your browser . 
```

## How To Run job

kubectl apply -f api-interaction-job.yaml
