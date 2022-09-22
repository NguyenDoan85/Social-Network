<h1 align="center">Social Network 💬</h1>

<p align="center">
    <img src="https://img.shields.io/github/repo-size/NguyenDoan85/Social-Network" />
    <img src="https://img.shields.io/github/languages/top/NguyenDoan85/Social-Network"  />
    <img src="https://img.shields.io/github/issues/NguyenDoan85/Social-Network" />
    <img src="https://img.shields.io/github/last-commit/NguyenDoan85/Social-Network" >
    </a>
</p>

<p align="center">
    <img src="https://img.shields.io/badge/Javascript-yellow" />
    <img src="https://img.shields.io/badge/MongoDB-blue"  />
    <img src="https://img.shields.io/badge/Mongoose-lightgrey" />
    <img src="https://img.shields.io/badge/Insomnia-orange" />
    <img src="https://img.shields.io/badge/Node.js-blue"  />
    <img src="https://img.shields.io/badge/Express.js-green" />
    <img src="https://img.shields.io/badge/Moment.js-teal" />
</p>

<p align="center">
    <img src="http://img.shields.io/badge/license-MIT-blue.svg"/>
</p>

## Table of Contents

- [Description](#description-🔍)
- [User Story](#user-story-💡)
- [Acceptance Criteria](#acceptance-criteria-🎯)
- [Installation](#installation-💾)
- [Technologies](#technologies-🔧)
- [Usage](#usage-💻)
- [Gif Demo](#Gif-Demo-🎞️)
- [License](#license-©️)
- [Contributing](#contributing-🧩)
- [Questions](#questions-❓)


## Description 🔍

- An application that used mysql database backend for an Social-Network site.

## User Story 💡

- AS A social media startup
- I WANT an API for my social network that uses a NoSQL database
- SO THAT my website can handle large amounts of unstructured data

## Acceptance Criteria 🎯

- GIVEN a social network API
- WHEN I enter the command to invoke the application
- THEN my server is started and the Mongoose models are synced to the MongoDB database
- WHEN I open API GET routes in Insomnia for users and thoughts
- THEN the data for each of these routes is displayed in a formatted JSON
- WHEN I test API POST, PUT, and DELETE routes in Insomnia
- THEN I am able to successfully create, update, and delete users and thoughts in my database
- WHEN I test API POST and DELETE routes in Insomnia
- THEN I am able to successfully create and delete reactions to thoughts and add and remove friends to a user’s friend list

## Installation 💾
- Clone the repo and use command `npm install` to install all require packages. 
- Require Insomnia to test the API ability.

## Technologies 🔧
- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Express.js](https://expressjs.com/)
- [Node.js](https://nodejs.org/en/)
- [MongoDB](https://www.mongodb.com/)
- [Mongoose](https://mongoosejs.com/)
- [Insomnia](https://insomnia.rest/)
- [Moment.js](https://www.npmjs.com/package/moment)

## Usage 💻

1. Input command npm start to start up the server. It will also created a database in mongoDB under the name `socialDB`.

<img src="./asset/start-server.jpg">

2. When API GET routes for users and thoughts are opened in Insomnia, the data for each of the routes is displayed in formatted JSON.

3. **User**, **Friend**, **Thought**, and **Reaction** routes are created to create the database and test the API on Insomnia.

4. **User Routes** - a user can create a user with a username and valid email address. When created, the user is assigned a unique user ID.

<img src="./asset/users.jpg">

- To create a user, click the `POST` request and enter the user's username and email address. Click Send.

- There are two `GET` requests that return user information. To return all users, click the `Find All Users` request, then click on Send. To return a single user, click the `Find User by Id` request. On the URL, enter the user's ID.

- To update a user by ID, click the `PUT` request. On the URL, enter the ID of the user whose information is going to be updated.

- To delete a user by ID, click the `DELETE` request and enter the user's ID.
- A message that reads, `"User and thoughts deleted!"` will appear if the user has been deleted from the database. If there is no such user or user ID in the system, the message, `"No user with this id!"` is shown.

- Click `Find All Users` to see if the user has been deleted.

5. **Friend Routes** - a user can add a friend and delete a friend.

- To add a friend, click the `POST` request. On the URL enter the user ID of the user who is adding a friend, then the user ID of the friend the user is adding. \*(Note: Please see the section on Tests for the API routes.)\*

- To see the user's friends, click `Find All Users`. The ID of the friends the user added are listed under `"friends"`. The `"friendCount"` indicates the number of friends the user added.

- To remove or delete a friend, click the `DELETE` request. On the URL enter the user ID of the user who is deleting a friend, then the user ID of the friend the user is deleting.

- To check if the friend has been removed from the user's friend list, click `Find All Users`.

6. **Thought Routes** - a user can create a thought, get all thoughts or a single thought by ID, update a thought by ID, and delete a thought by ID.

- To create or add a thought, click the `POST` request. Enter the `"thoughtText"`, `"username"`, `"userID"` of the user creating the thought.

- To get all thoughts, click the `GET All Thoughts` request. All the thoughts that were created will appear, as well as the date and time they were created. Each created thought is assigned a unique thought ID. Click `GET All Users` to access the thought ID.

- To get a thought by ID, click the `GET Thought by Id` request and enter the thought ID.

- To update a thought, click the `PUT` request. On the URL, enter the thought ID. Enter the necessary changes on the text body. To see the changes, click `GET All Thoughts`.

- To delete a thought by ID, click the `DELETE` request. On the URL, enter the thought ID that will be deleted.

- When the thought is successfully deleted, the text can no longer be found when you try to access it by clicking `GET All Thoughts.` The thought ID is also deleted when you click `Find All Users.`

7. **Reaction Routes** - a user can create a reaction and delete a reaction.

- To create a reaction, click the `POST` request. On the URL, enter the ID of the thought the user is reacting or commenting on. Then enter the `"reactionBody"` and `"username"` of the user creating the reaction.

- Click on `GET All Thoughts`to see the reaction, the username of the user who created the reaction, the reaction ID, date and time the reaction is created, and the user's reaction count.

- To delete a reaction, click the `DELETE` request. On the URL, enter the ID of the thought the user created a reaction or commented on, then the reaction ID.

- The message, `"No thought with this id!"` will appear when a reaction is deleted or a reaction is not associated with a user ID.

8. MongoDB - After creating data on Insomnia, MongoDB also reflects the same data and changes that were made:

## Gif Demo 🎞️
![Demo](./asset/Demo.gif)

## License ©️
✏️ This project is license under MIT

## Contributing 🧩

Please refer to "Fork" or be assigned by Owner.

## Questions ❓

If you have any questions about this project, please contact me directly at ericdoan2008@gmail.com. You can view more of my projects at https://github.com/NguyenDoan85.

## Author 🎊

- This app created by me, please follow my [Github](https://github.com/NguyenDoan85) for more cool app. 
- Here is my [Linkedin](https://www.linkedin.com/in/eric-doan-80547b86/)!