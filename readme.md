# E-Commerce Back End Program

# User Story    
    AS A manager at an internet retail company
    I WANT a back end for my e-commerce website that uses the latest technologies
    SO THAT my company can compete with other e-commerce companies

# Acceptance Criteria
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

# Getting Started
    You must install the following packages

        npm install mysql2
        npm install sequelize
        npm install dotenv

# Database Models 
    # Category - ID, Integer, Doesn't allow null values, set as primary key, uses auto increment, category_name, string, doesnt allow null values.

    # Product - ID, Integer, Doesn't allow null values, set as primary key, uses auto increment, category_name, string, doesnt allow null values.

    # Tag - ID, Integer, Doesn't allow null values, set as primary key, uses auto increment, tag_name, string.

    # ProductTag - ID, Integer, Doesn't allow null values, set as primary key, uses auto increment, product_id, integer, references the product model's id, tag_id, integer, references the tag model's id. 

# Associations 
    Association methods on your Sequelize models , used o create the following relationships between them:

        # Product belongs to Category, as a category can have multiple products but a product can only belong to one category.

        # Category has many Product models.

        # Product belongs to many Tag models. Using the ProductTag through model, allow products to have multiple tags and tags to have many products.
        
        # Tag belongs to many Product models.


# Seed the Database
        fter creating the models and routes, run 'npm run seed' to seed data to your database so that you can test your routes.

# Sync Sequelize to the Database on Server Start
        Create the code needed in server.js to sync the Sequelize models to the MySQL database on server start.
        
# Walkthrough Video