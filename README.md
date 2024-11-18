# Clone the repositary

git clone https://github.com/MarckoAbhi/Chat-App.git

# Navigate to backend folder and install dependencies:

cd backend

npm install

## Now go to root directory
cd ..

# Navigate to the frontend folder and install dependencies:

  cd frontend
  
  npm install

# Environment Variable 

## in backend directory create a .env file and write this code to there 

PORT=4002

MONGODB_URI=mongodb+srv://<your_mongodb_user >:<your -passwoed>@cluster0.tyt0d.mongodb.net/<your_database_name>?retryWrites=true&w=majority&appName=Cluster0

JWT_TOKEN=


## To create your own database going to mongodb compass and login there after login you create a new project .
## After that create deployment and now create cluster 
## After creating cluster click on connect and click on driver 
## there you can see your monogoDB url , copy and paste in your env file MONGODB_URI= 

## To find JWT_TOKEN you can click on dropdown button at + button in your vs code terminal and click on Git Bash
## Now you type this CMD

openssl rand -base64 32 

# now you find yor JWT TOKEN Copy and paste it in your .env file

#  Running Application 
## for Backend

cd Backend

npm start

## For frontend

npm run dev

## open your browser and go to http://localhost:3001
## server is running on http://localhost:4002


# Acknowledgement

React.js

Node.js

MongoDB

Socket.io


Socket.io
