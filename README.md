# setting-up-sequelize

## Step One: Set up file tree skeleton 
1) Create empty file structure (README.md,.gitignore, server.js, /db folder with schema.sql and seeds.sql, /routes folder with api-routes.js and html-routes.js, views or public folder with handlebars/html, css/css.styles. js/app.js)
## Step Two: Set up npm packages
2) Run npm init or npm init -y, Install the following packages:
-npm i mysql, npm i mysql2, npm i express, npm i express-handlebars, npm i sequelize.
Run npm i
## Step Three: Set up Config and Models folder with sequelize file generator
Run sequelize init:models & sequelize init:config in terminal (make sure to run npm install -g sequelize sequelize-cli to install sequelize globally)
### Step Three A) : Set up config.json file
in the generated /config folder open config.json and modify the development object's "database","username" and "password" values to match your MYSQL database.
### Step 3 B) : Set up models.js files for database objects
Navigate to the models folder and create a new file that matches the main object of your project ( example todolist.js.) Create a model file with columns for "text" (DataTypes.STRING), and "complete" (DataTypes.BOOLEAN).
Example code:
module.exports = function(sequelize, DataTypes) {
  var Todo = sequelize.define("Todo", {
    text: DataTypes.STRING,
    complete: DataTypes.BOOLEAN
  });
  return Todo;
};
Set up a new model file for each object in database.

## Step Four: 
