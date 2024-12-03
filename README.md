
# Docker Image For Chat app

[Introduction]
This Project is a real time chat app built using MERN (MongoDB, Express, React, Node.Js) Stack.
It provide basic functionalities to assist user to signup.






# Tech Stack

**Client:** React.js tailwind for styling
Socket.io

**Server:** Node, Express, MongoDB

**Docker Image** Docker Desktop, Kubernetes, minikube





## Features

- Signup and Login,
- Chat to other 
- Logout



## Installation


## Windows:

Download Docker Desktop from Docker's official website.

```bash
 https://docs.docker.com/desktop/setup/install/windows-install/
```

 First install chocoloty run this CMD in POWERSHELL
```bash
 Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
 "Install Kubernetes"Installation


 ```bash
 choco install kubernetes-cli
```


# Backend Environment Variable setup

PORT=4002

MONGODB_URI=mongodb+srv://<your_mongodb_user >:<your -passwoed>@cluster0.tyt0d.mongodb.net/<your_database_name>?retryWrites=true&w=majority&appName=Cluster0

JWT_TOKEN=

### To create your own database going to mongodb compass and login there after login you create a new project .
### After that create deployment and now create cluster 
### After creating cluster click on connect and click on driver 
### There you can see your monogoDB url , copy and paste in your env file MONGODB_URI= 

### To find JWT_TOKEN you can click on dropdown button at + button in your vs code terminal and click on Git Bash
### Now you type this CMD


```bash
 openssl rand -base64 32 
```

## Now Copy and paste it in your .env file

# To pull the backend  and frontend  docker image run this cmd

```bash
 docker pull marckostar7321/chat-app-backend:v1
```

```bash
 docker pull marckostar7321/chat-app-frontend:v1
```



## Run Locally

Clone the project

```bash
  git clone https://github.com/MarckoAbhi/MernAppDocker.git
```

In root directory run this cmd 

```bash
  docker build -t marckostar7321/chat-app-backend:v1 -f Backend/Dockerfile . 
```
```bash
  docker build -t marckostar7321/chat-app-frontend:v1 -f Frontend/Dockerfile . 
```

Start the server

```bash
  docker run -p 3001:80 marckostar7321/chat-app-frontend:v1
```
```bash
  docker run --env-file ./Backend/.env -p 4002:4002 marckostar7321/chat-app-backend:v1
```




## Running Tests

## To see deployments and services Run these CMD

```bash
  kubectl get deployments
```
```bash
  kubectl get services
```

Server is running on 
port no 4002

Frontend is running on port 80
