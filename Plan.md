- first to start the backend
- npm init
- description evangadi forum
- entry point server.js
- author anteneh
- automatically it creates our package.json
- create server.js file based on package.json main
- intall npm i cors, npm i express
- then create a server using express and create a middleware using cors
- app.use(express.urlencoded({ extended: true })); when we say urlencoded mean we want to use a file or any thing that comes from the frontend
- and also app.use(express.json()); whatever comes change it to JSON
- to check the git (ls -al) command
- to see (master) go initiate using - git init
- next step I want to hide my port number
- to hide our port we write on .env file PORT=4000
- then we are going to proces that port what we write on .env 0n server.js file const port = process.env.PORT;
- and to get functionality of .env install npm i dotenv
- and import file of dotenv
- and our .env files we don't want it to track so we create .gitignore file
- on .gitignore file we write what we want to untrack node_modules and .env
- then go to our databse and create a new databse and user
- then use npm i mysql or npm i mysql2
- then connect to the database by importing mysql on databse.js
- then create a folder called server, inside server folder cretare two folder api and config
- on config we have databse.js and on api folder we have users folder
- connect my database.js to server.js
- create tables such like answer, profile, registration and question
- next step how do we insert in to
- on api create folder stands for user
- user.service.js i use for install/inserting then connect to the database by importing
- and export each modules
- user.router.js uses for routing
- user.controller.js uses for controlling and insert(controll the data like validation)
- to hash my password install this npm i bcryptjs
- after registration finished grap userId and pass to the profile
- before going to postman make the routing
- we get routing from express
- status code 500 is known as the "Internal Server Error."
- Status Code 200 - OK:
  -Status Code 200 - OK:
  This status code indicates that the client's request was successful. The server has fulfilled the request and is sending the expected data back to the client. For example, when you load a webpage successfully, you will often receive a 200 OK status code.

- Status Code 400 - Bad Request:
  The 400 status code indicates that the server could not understand the client's request due to a problem with the request itself. It could be due to missing or incorrect parameters, invalid syntax, or other client-side errors. The client should modify its request and try again.

- Status Code 404 - Not Found:
  A 404 status code indicates that the requested resource was not found on the server. This could be due to a mistyped URL or a resource that has been moved, deleted, or is otherwise inaccessible. It's one of the most common errors encountered when browsing the web.

- status code 500 is a server error response code. It indicates that the server encountered an unexpected condition that prevented it from fulfilling the request made by the client (usually a web browser or another application).

- download Token npm i jsonwebtoken then import jwt
- to make run frontend and backend at the same time intall this (npm i concurrently) at the backend package.json
- then we write some scripts at the backend package.json
  "dev":"concurrently \"nodemon server.js\" \"npm run client\"",
  "client": "npm start --prefix client",
  "start": "node server.js"
- and we will run always from the backend
- so we use to start both npm run dev

- inspect then go to Application go to localStorage
- to get auth-token it store for 1 hour after one hour it expire
- install npm i axios and import axios from 'axios'; on app.js

- then install npm i react-router-dom

