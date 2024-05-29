# Books API

## Description

**It is build to perform basic CRUD operations using REST API**

## Usage

To test the api routes in Postman, use can use this endpoints

```sh
Base Url: https://book-easy-server.vercel.app/api
```

**For all requests set the Content-Type in header as application/json and send data in json format**

1. Authentication Rotes

   These routes helps to login and register user to the website

- **Register**

Method: **POST**

      Route: /auth/register

example data {
"name":"dummy",
"email": "dummy@gmail.com",
"password": "passwordummy"}

- **Login**

Method: **POST**

    Route: /auth/register

example data
{
"email": "email@gmail.com",
"password":"desiredPassword"
}

**Set this code in Postman to automatically add token for futher routes**

Open Tests and paste this code 

```sh
const data = pm.response.json()  pm.globals.set("accessToken", data.token)
```
Open Authorization and set Type to 
```sh
Bearer Token 
```

2. Manipulate User

- **Get User**

Method: **GET**

        Route: /user:userId


- **Update User**

Method: **PUT**

        Route: /user:userId

example data {
    "name": "updatedName"
}

- **Logout User**

Method: **GET**

        Route: /user:userId


- **Delete User**

Method: **DELETE**

        Route: /user:userId

## SetUp/Installation
 Clone the repository using `git clone repository-link` and install dependencies using `npm install` command

Use the sample env file to know the required the envirnomental varabiles for this project

Create your own environemet varaibles

- MongoDBConnection Url
- JWT_SECRET 
- RAZORPAY_KEY_ID
- RAZORPAY_KEY_SECRET