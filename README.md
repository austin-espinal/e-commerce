# e-commerce

## Description 

This project was created to provide a back-end for a e-commerce retail website. It allows you to view by categories, products, and tags. You are also able to create, update, and delete categories, products, and tags. The application uses Javascript, Node, and MySQL.

## Table of Contents

* [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
* [Tests](#tests)
* [Questions](#questions)

## Installation

You'll need to install MySQL for the project which instructions can be found at (https://dev.mysql.com/doc/mysql-installation-excerpt/5.7/en/)

Also you will need to install Insomnia for the project which can be found at (https://docs.insomnia.rest/)

After downloading and extracting the project from the zip, open the terminal and install these node packages

* npm init -y
* npm i dotenv express
* npm i mysql2 sequelize

Make sure to duplicate the .env.EXAMPLE file first, then rename the duplicate as ".env". The user and password in the .env should match your MySQL user and password in order to use the application/ run the server.

The database needed for the application will need to be set up as well. First, log into MYSQL via the terminal using "mysql -uroot -p". Enter in your password and type in "SOURCE db/schema.sql" when MYSQL is connected to create the ecommerce_db database. Exit MYSQL shell by typing in "quit;". Next, start the server by typing "npm start" in the terminal to set up the tables for the database then press CTRL + C and type "Y" to stop the server. After, you will want to populate the database with data via seeding. Type "npm run seed" in the terminal to seed the database. Now the application is ready to be used.

## Usage 

(https://watch.screencastify.com/v/QTkpRx3LGjrXerky5eRI)
The link above is a link to the application direction video/showcase

Start the server by typing "npm start". Then use Insomnia to try the each of the routes.

Category:
USE localhost:3001/api/categories
-GET FindAll: it will show all categories in the database.
-POST Create: allows you to create a new category. must put in json format.
example {
           "category_name": "Sandals"
        }

USE localhost:3001/api/categories/:id
-GET FindOne: it will show the category by the id specified by you.
-PUT Update: it will update the catergory by the id specified by you. must put in json format.
-Delete: it will delete the catergory by the id specified by you.

Product:
USE localhost:3001/api/products
-GET FindAll: it will show all products in the database.
-POST Create: allows you to create a new product. must put in json format.
example {
           "product_name": "Basketball",
           "price": 200.00,
           "stock": 3,
           "tagIds": [1, 2, 3, 4]
        }

USE localhost:3001/api/products/:id
-GET FindOne: it will show the product by the id specified by you.
-PUT Update: it will update the product by the id specified by you. must put in json format. use exact scheme in POST example to update.
-Delete: it will delete the product by the id specified by you.

Tag:

USE localhost:3001/api/tags
-GET FindAll: it will show all tags in the database.
-POST Create: allows you to create a new tag. must put in json format.
example {
           "tag_name": "orange"
        }

USE localhost:3001/api/tags/:id
-GET FindOne: it will show the tag by the id specified by you.
-PUT Update: it will update the tag by the id specified by you. must put in json format.
-Delete: it will delete the tag by the id specified by you.

## Contributing

No contribution necessary.

## Tests

You can test this application by seeding the database using "npm run seed" then testing out each route using Insomnia. You can also populate the database by creating categories, products, and tags through the post/create routes via Insomnia.

## Questions

Github: [austin-espinal](https://github.com/austin-espinal)   
Email: [austinespi@gmail.com](mailto:austinespi@gmail.com)  

The best way to reach me is through email. Github is also acceptable.