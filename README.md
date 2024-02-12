# PWP SPRING 2024

# PROJECT NAME
Chat application

# Group information

- Student 1. Hung Trinh (htrinh23@student.oulu.fi)
- Student 2. Mazen Hassaan (Mazen.Hassaan@student.oulu.fi)
- Student 3. Toseef Ahmed
  (Toseef.Ahmed@student.oulu.fi)
- Student 4. Saim Akhtar (saim.-@student.oulu.fi)

**Remember to include all required documentation and HOWTOs, including how to create and populate the database, how to run and test the API, the url to the entrypoint and instructions on how to setup and run the client**

# Chat Application

## Description

Chat application developed using [Nest](https://github.com/nestjs/nest) framework and TypeScript.

In backend site, we use Mongoose, which is a Node.js-based Object Data Modeling (ODM) library for MongoDB. It is akin to an Object Relational Mapper (ORM) such as SQLAlchemy for traditional SQL databases.

## Code Repository

Clone the code from [This Repository](https://github.com/Abouelhassen/PWP-CtrlShiftElite) using the commmand

```bash
git clone https://github.com/Abouelhassen/PWP-CtrlShiftElite
```
## Installation
After you have cloned the repository, Navigate to PWP-CtrlShiftElite using

```bash
cd PWP-CtrlShiftElite
```

Run

```bash
npm install
```

This will install the dependencies as defined in **_Package.json_** file.

## Running the app

As of now, we have only created the Database schema, so you do not need to run the entire application. We have provided a **dbdump.js** file which you can use to populate data into MongoDB.

In order to create the database and dump data into collections, you need following tools.


1.  MongoDB Client. (Installed when you run ```npm install```)
2.  Docker. [(Here)](https://www.docker.com/products/docker-desktop/#)
3.  Docker Compose file. (Provided in the code repository.)
4.  **dbdump.js** file. (Provided in the root directory of the code repository.)
5.  MonngoDB Compass [(Here)](https://www.mongodb.com/try/download/compass) or Studio 3T [(Here)](https://studio3t.com/download/)

Once you are in the root directory of the project, run

```bash
$ docker-compose up -d
```

This will setup a database in the docker container.

Once it is created, run

```bash
$ node dbdump.js
```

Open MongoDB Compass or Studio 3T (Whichever you have downloaded), and create a new connection using following parameters.

1.  **Host:** localhost
2.  **PORT:** 27017
3.  **DB_NAME:** chatapp
4.  **username:** rootuser
5.  **password:** rootpass

Here is the connection string that you may use in the connection manager.

```bash
mongodb://rootuser:rootpass@localhost:27017/admin
```

Once you are logged in, you would be able to view the collections and data inside them.

Here is the ER diagrams of the database:
![alt text](images/ERD.png)


