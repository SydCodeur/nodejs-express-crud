# nodejs-crud-api
Node.js, Express and MongodB: Create a Restfull API with images upload

## What will you learn ?
What will you learn by downloading my code?
- Use of **express** to make API creation simple
- Using **mongoose** to manage communication with Mongo DB
- Image Upload with **multer**
- Image deletion with the notions of paths and file system in node
- Field validation using **express-validator**
- Creation of reusable methods thanks to the concept of **modules**
- Creation of a functional REST API with Node.js, Express and Mongo DB.

Are you ready ? Let's go

## Step 1: Installing dependencies

Clone the repository then run **npm install**

## Step 2: Create .env file
Create a file named .env at the root of your project and add the following content:
  #### For MongoDB Atlas:
  ```properties
  MONGODB_URL=mongodb+srv://<username>:<password>@cluster0.eox3j.mongodb.net/player-db?retryWrites=true&w=majority
  PORT=3000
  ```

  Replace <username> and <password> with your actual MongoDB Atlas credentials. The database name (player-db) is specified in the URL.

   #### For local MongoDB:
   ```properties
  MONGODB_URL=mongodb://localhost:27017/player-db
  PORT=3000
  ```

  This file provides your API with the necessary details to connect to MongoDB. Choose the appropriate configuration based on your environment.

## Step 3: Launch your project

To launch your project, just type the following command : **node app.js**. Your API will therefore run on port 3000

## Step 4: Test the API endpoints

This is an API that manages players (football for example). A player is characterized by:
* name: the name of the player
* age: the player's age
* bio: a brief biography of the player (at least 15 characters)
* photoUrl: player photo
* createdAt and updatedAt are generated automatically using the **timestamps: true** statement in the **models/player.js file**

So we have a total of 5 routes

1. Add player http://localhost:3000/api/v1/player
2. List of all players http://localhost:3000/api/v1/players
3. Find player by Id http://localhost:3000/api/v1/player/:playerId
4. Update player http://localhost:3000/api/v1/player/:playerId
5. Delete player http://localhost:3000/api/v1/player/:playerId

## Some precisions

* When you add a player their photo is placed in the /images folder (make sure to create this folder at the same level as the controllers folder if it doesn't exist).
* I delete player image if this image was replaced during the update (or if the player was deleted)
* In the utils/syd-functions.js folder you will find reusable functions in the controllers/player.js

## Examples of API tests with postman (in pictures)

* Add Player

<img src="https://i.ibb.co/TqTVxsn/add-player.png" alt="add-player" border="0">

* List of players
<img src="https://i.ibb.co/RSgvjLt/list-of-players.png" alt="list-of-players" border="0">

## Documentation

For a comprehensive overview of the API endpoints and to test the API, please refer to our documentation : https://documenter.getpostman.com/view/16446301/2sAYXBEeV5#c7c23cc9-2dbd-499e-abde-d443127a317b

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these guidelines:

1. Fork the repository.
2. Create a new branch for your feature or bugfix: `git checkout -b feature/your-feature-name`.
3. Make your changes and ensure the code passes all tests.
4. Commit your changes with a clear commit message.
5. Push to your branch: `git push origin feature/your-feature-name`.
6. Open a pull request describing your changes in detail.

Please ensure your contributions respect the project's coding style and include appropriate tests where applicable.
