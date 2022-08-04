# E-commerce-Backend-Application
## License
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
## Table of Contents
  - [Description](#description)
  - [Application Demo](#application-demo)
  - [Installation](#installation)
  - [Usage](#usage)
    - [Code Examples and Screenshots](#code-examples-and-screenshots)
  - [Contributing](#contributing)
  - [License](#license-1)
  - [Tests](#tests)
  - [Technologies Used](#technologies-used)
  - [Questions](#questions)
## Description
Challenge is to build the back end for an e-commerce site.This application was build by Express.js API and configure it to use Sequelize to interact with a MySQL database.When the my server is started and the Sequelize models are synced to the MySQL database.We need to fill Out the API Routes to Perform RESTful CRUD Operations
GET routes to return all categories, all products, and all tags.
GET routes to return a single category, a single product, and a single tag .
POST, PUT, and DELETE routes for category,products and tags.


[Solution URL](https://github.com/ashachakre0906/E-commerce-Backend-Application)
## Application Demo
![Live Demo](./public/assets/images/ecommbackendapp.gif)

[Screencastify link](https://watch.screencastify.com/v/mwtQKfVpc1W25CZnSCrQ)

<img src = "/public/assets/images/getallcategories.png" alt = "GET all categories">

<img src = "/public/assets/images/getoneproductbyid.png.png" alt = "GET one product by id">
<img src = "/public/assets/images/postcategory.png" alt = "Create new category">
<img src = "/public/assets/images/puttag.png" alt = "Updating new tag">

## User Story
```
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```
## Acceptance Criteria
```
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia Core for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia Core
THEN I am able to successfully create, update, and delete data in my database
```
## Installation
* Install Node in your computer by going to `https://nodejs.org/en/download/`
* Create .gitignore file before installing any npm dependencies and include node_modules/ and .DS_Store/ and .env/ so that the directory isn't tracked or uploaded to GitHub.
* Create a new github repository and clone it to your local machine.
* Navigate to the repo which you just created by typing`cd` command  and open it in your code editor by typing the command in your terminal `code .`
* `npm i` to install the `node_modules`
* `dotenv` package to use environment variables to store sensitive data, like your  MySQL username, password, and database name.
* Following packages needed to to connect your Express.js API to a MySQL database 
  - `MySQL2` 
  - `Sequelize` 
* run `npm run seed` to seed data to your database so that we can test our routes.
* Sync Sequelize to the Database on Server Start.
  - `nodemon server.js`

## Usage
### Code Examples and Screenshots
***This is how we set up fields and rules for ProductTag model***
```
ProductTag.init(
  {
    id: {
      type: DataTypes.INTEGER,
      allowNull: false,
      primaryKey: true,
      autoIncrement: true,
    },

    product_id: {
      type: DataTypes.INTEGER,
      references: {
        model: "product",
        key: "id",
      },
    },
```

***PUT route which updates a category by its `id` value***
```
router.put('/:id', async(req, res) => {
  // update a category by its `id` value
  try {
    const updateCategory = await Category.update(req.body,{
      where:{
        id: req.params.id,
      },
    });
  if (!updateCategory[0]) {
     res.status(404).json({message: 'No category with this id!'});
     return;
    }
    res.status(200).json(updateCategory);
  } catch (err) {
    res.status(500).json(err);
  }

});

```
## Tests
GET, POST,PUT AND DELETE for Categories,Products and tag routes being tested in Insomnia Core.
## License
This project is license under [Apache](https://choosealicense.com/licenses/apache/)

## Technologies Used
![Sequelize Badge](https://img.shields.io/badge/Sequelize-magenta.svg)
![Express.js Badge](https://img.shields.io/badge/Express-purple.svg)
![Javascript Badge](https://img.shields.io/badge/Javascript-blue.svg)
![Node.js Badge](https://img.shields.io/badge/Node-yellow.svg)
![mysql2 Badge](https://img.shields.io/badge/mysql2-orange.svg)

## Questions
if you have any questions please reach out to me:<br>
Email Address: chourpagar.asha@gmail.com <br>
Github Repo URL:[GitHub](https://github.com/ashachakre0906)



