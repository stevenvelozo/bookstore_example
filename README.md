# Book Store Example

Example Book Store App for the Meadow and Meadow Endpoints Talk.

# How to use:

## Install MySQL or MariaDB on your computer

I recommend using docker!

## Create a Database in MySQL

I recommend calling this `bookstore` so everything works as-is.

## Update the `api/bookstore-configuration.json` MySQL section to match your user

You need to make sure the IP, port, user and password are all correct.

## Install the Node.js modules

From the `api/` folder, run `npm install`.  Make sure to user node version 8.

## Run the Stricture database description generation scripts.

You can run `Build-Database.sh` from the `api/` folder and everything will generate properly

## Create the Database Tables

From your favorite MySQL client, connect to the server you are already running on your computer.  Load up the file stricture generated in `api/model/sql_create/BookStore-CreateDatabase.mysql.sql` and execute it against your database.  This will create all the empty tables you need.

## Run the API server

If everything went well so far, you should be able to go to the `api` folder and run `npm start`.

## Import the books to the database

From a terminal, navigate to the `api/` folder and run `node import-books.js`

A bunch of spam will happen on the terminal as books, authors and their connections are loaded.

## Point a browser at http://127.0.0.1:8080/

What a well-stocked bookstore!
