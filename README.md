# Clone the repositary

git clone https://github.com/MarckoAbhi/MernAppDocker.git

### Navigate to backend folder and install dependencies:

cd backend

npm install

## Now go to root directory
cd ..

### Navigate to the frontend folder and install dependencies:

  cd frontend
  
  npm install

# Environment Variable 
## In backend directory create a .env file and write this code to there 

PORT=4002

MONGODB_URI=mongodb+srv://<your_mongodb_user >:<your -passwoed>@cluster0.tyt0d.mongodb.net/<your_database_name>?retryWrites=true&w=majority&appName=Cluster0

JWT_TOKEN=

### To create your own database going to mongodb compass and login there after login you create a new project .
### After that create deployment and now create cluster 
### After creating cluster click on connect and click on driver 
### There you can see your monogoDB url , copy and paste in your env file MONGODB_URI= 

### To find JWT_TOKEN you can click on dropdown button at + button in your vs code terminal and click on Git Bash
### Now you type this CMD

openssl rand -base64 32 

## Now you find yor JWT TOKEN Copy and paste it in your .env file

## Running Application 
### For Backend

cd Backend
npm start

### For frontend

npm run dev

### Open your browser and go to http://localhost:3001
### Server is running on http://localhost:4002

## Acknowledgement
React.js
Node.js
MongoDB
Socket.io

## To creating Docker image Run these CMD- 
cd Frontend
npm run build
cd.. 

### In root directory run this cmd 
docker build -t your docker username :v1 -f Fackend/Dockerfile . 

docker build -t your docker username :v1 -f Backend/Dockerfile .

### To push your image on docker hub run this cmd
docker push your username -backend:v1 

docker pushyour username -fackend:v1

### Like this- docker push marckostar7321/chat-app-backend:v1 
## Compose up 
docker-compose up --build   
docker-compose down

### To run docker frontend image and backend image -

docker run -p 3001:80 marckostar7321/chat-app-frontend:v1

docker run --env-file ./Backend/.env -p 4002:4002 marckostar7321/chat-app-backend:v1

### Open your browser and go to http://localhost:3001
### Server is running on http://localhost:4002

## To run kubernetes deployments and services use these CMD

kubectl apply -f backend-deployment.yaml

kubectl apply -f frontend-deployment.yaml


## To see deployments and services Run these CMD

kubectl get deployments

kubectl get services


