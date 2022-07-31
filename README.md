# E-Commerce Manager

E-Commerce Manager provides APIs to manage products in the stock and search them by tags and categories.

Click [here](https://drive.google.com/file/d/196rigeKhHgBDy6WwqW--K9HWgCxuljxW/view) for a quick demo of the application.

![Notes page](/assets/images/ecommerce-manager.png)


## Table of Contents

* [Installation](#installation)

* [Usage](#usage)

* [Built With](#built-with)


## Installation

After cloning the repo, run `npm i` from the cloned directory to install node dependencies. 
Next, setup make a copy of `.env.EXAMPLE` as `.env` file and update the port, database name, user and password. You'll also need to install mysql to get the database working.

To use the application locally, run `node server.js` in your CLI, and then open `http://localhost:3001` in your preferred browser.


## Usage

First, create the database by running `mysql schema.sql` from termincal. Optionally, run `npm run seed` to insert dummy data for data.

Once you have the database initialized, run `npm run start` to start the server.
The application provides the following APIs with GET, POST, PUT and DELETE methods to retreive, create, update and delete:

Categories: /api/categories/
Products: /api/prodcuts/
Tags: /api/tags/

Additionally, The application provides following APIs:
/api/categories/<category_id> to look up a sepcific category and products in it.
/api/prodcuts/<product_id> to look up a sepcific product.
/api/tags/<tag_id> to look up a sepcific tag and products with the tag.


## Built With

The application is build on top of Node.js. It uses Express.js for running the server and routing, dotenv for environment variables, sequelize for ORM and mysql for underlying database.