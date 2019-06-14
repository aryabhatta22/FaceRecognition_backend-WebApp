#Before you run local server

you need to create a database table where all the information of user will be saved

1. Download postgreSQL here: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
2. Install postgreSQL. During installation set password to 'unitedwestand' (without quotes) or if you want to keep your own password -
        2.1 Open server.js in editor.
        2.2 Go to function knex and change value of attribute password ( by default in line 15 ).
3. Add environment variable of bin folder ( usually C:\Program Files \PostgreSQL\10\bin  )       
4 .Go to terminal and run following commands:

        => psql -U postgres
                (enter the password )
        => CREATE DATABASE face_recognition;
        => \c face_recognition
        => CREATE TABLE users  (
                id serial PRIMARY KEY,
                name VARCHAR(100),
                email text UNIQUE NOT NULL,
                enteries BIGINT DEAFULT 0,
                joined TIMESTAMP NOT NULL
        );
        => CREATE TABLE login  (
                id serial PRIMARY KEY,
                hash VARCHAR(100) NOT NULL,
                email text UNIQUE NOT NULL
        );
        => \q

#How to run?

if you dont have Nodejs installed, install it from here https://nodejs.org/en/download/

1. Clone the repository
2. open repository in terminal and run "npm install" (without quotes).
3. Now run "npm start" (without quotes).

Server will start. 

For Face Detection fronend : https://github.com/aryabhatta22/FaceRecognition_frontend-WebApp
                                Or 
Test database using Postman :https://www.getpostman.com/downloads/

NOTE: If face is not being detected, you might need clarifai API key for face recognition, if so get free api key from here : 
        https://www.clarifai.com/models/face-detection-image-recognition-model-a403429f2ddf4b49b307e318f00e528b-detection
        
