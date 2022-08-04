# E-commerce-Backend-Application
# team-Profile-Generator
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
<!-- ![Live gif](/dist/assets/images/team-profile.gif) -->

<!-- [Screencastify link](https://drive.google.com/file/d/1X7fo16XXLiZs6Yr8Qc6COQTPitZe7FGh/view?usp=sharing) -->

***The following image shows the generated HTML’s appearance and functionality in large screen***
<img src = "/dist/assets/images/team-profile.png" alt = "image of team profile">

***The following image of a webpage is Responsive you can shrink the size and set the appropriate responsive breakpoints***

<img src = "/dist/assets/images/team-profile-responsive.png" alt = "image of team profile">

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
***Function generateCards() will generate the cards dynamically for Manager,Employee and Intern through forloop***
```
function generateCards(data) {
  for (let i = 0; i < data.length; i++) {
    if (data[i].getRole() == "Manager") {
      let str = `
         <div class="card mb-3" style="max-width: 18rem;">
            <div class="card-header"><h3>${data[i].getName()}</h3><i class="fa-solid fa-mug-hot"></i> Manager
            </div>
            <div class="card-body text-dark">
              <h5 class="card-title"></h5>
              <p class="card-text"></p>
              <ul class="list-group">
                <li class="list-group-item">id: ${data[i].getId()}</li>
                <li class="list-group-item">Email: <a href = "mailto:${data[i].getEmail()}">${data[i].getEmail()}</a></li>
                <li class="list-group-item">Office number: ${data[i].getOfficeNumber()}</li>
              </ul>
            </div>
         </div>
    `;
      cards += str;
```
## Tests
Our application is using Jest package for running the suite of unit tests.In order to run jest tests for Employee,Engineer,Intern and Manager classes we need to enter the following command in the terminal.All the tests must PASS.
```
npm run test
```
## Contributing
not applicable at this time.
## License
This project is license under [MIT](https://choosealicense.com/licenses/mit/)
## Technologies Used
![HTML Badge](https://img.shields.io/badge/HTML-orange.svg)
![CSS Badge](https://img.shields.io/badge/CSS-purple.svg)
![Javascript Badge](https://img.shields.io/badge/Javascript-blue.svg)
![Node.js Badge](https://img.shields.io/badge/Node-yellow.svg)
![Inquirer Badge](https://img.shields.io/badge/Inquirer-orange.svg)
![Bootstrap Badge](https://img.shields.io/badge/Bootstrap-darkblue.svg)
![Jest Badge](https://img.shields.io/badge/Jest-grey.svg)

## Questions
if you have any questions please reach out to me:<br>
Email Address: chourpagar.asha@gmail.com <br>
Github Repo URL:[GitHub](https://github.com/ashachakre0906)



