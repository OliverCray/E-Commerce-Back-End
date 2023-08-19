# E-Commerce-Back-End

## Purpose of Task

Creation of a back-end for an e-commerce site that will use Sequelize to communicate with a MySQL database. The user will be able to create, read, update and delete Products, Categories and Tags using tools like Postman or Insomnia. This application will make use of Node.js, express.js, MySQL, Sequelize and dotenv.

## Table of Contents

- [User Story](#user-story)

- [Acceptance Criteria](#acceptance-criteria)

- [Problems Solved](#problems-solved)

- [Usage](#usage)

- [Demonstration Video](#demonstration-video)

## User Story

```md
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```

## Acceptance Criteria

```md
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete data in my database
```

## Problems Solved

- The user is able to connect to the database using Sequelize by adding the required information to a .env file
  - The required information is outlined in the included **.env.EXAMPLE** file
- The user is able to create and seed a development database by entering the schema and seed commands
- When the user invokes the application, the server starts and the Sequelize models and synced to the MySQL database
- The user is able to access GET, POST, PUT and DELETE API routes for products, categories and tags
  - POST, PUT and DELETE requests respectively create, update and delete data in the database

## Usage

After cloning the repository, navigate to the folder using the terminal and type the following command to install the required dependencies for this application.

```sh
npm i
```

Rename the **.env.EXAMPLE** file to **.env** and input your details, these will be the same details you use to login to the MySQL shell.

```dosini
DB_NAME='ecommerce_db'
DB_USER=''
DB_PASSWORD=''
```

To create the database, first login to the MySQL shell by typing the following command in the terminal, enter your password when prompted.

```sh
mysql -u root -p
```

You now need to create the database using the source command, after which you can exit the MySQL shell using the quit command.

```sh
source db/schema.sql
```

```sh
quit;
```

To seed the database, type the following command in the terminal.

```sh
npm run seed
```

To run the application, type the following command in the terminal.

```sh
npm start
```

You can then use tools like Postman or Insomnia to send requests to the API.

- [Postman](https://www.postman.com/downloads/)

- [Insomnia](https://insomnia.rest/download)

## Demonstration Video

A demonstration video is availabe [here](https://drive.google.com/file/d/1AeMzXNTJbDME81XdugvIjCQyXMpJ82Ac/view)
