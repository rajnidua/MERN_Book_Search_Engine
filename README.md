# MERN_Book_Search_Engine

This app allows you to search for new books, create a list of searched books to purchase.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

# Overview

```md
Setting up an Apollo Server to use GraphQL queries and mutations to fetch and modify data, replacing the existing RESTful API.

Modifying the existing authentication middleware so that it works in the context of a GraphQL API.

Creating an Apollo Provider so that requests can communicate with an Apollo Server.

Deploying your application to Heroku with a MongoDB database using MongoDB Atlas.
```

# Deployed App

https://aqueous-taiga-47604.herokuapp.com/

![](./workingApp1.gif)

![](./workingApp2.gif)

# Installations

npm install

# Deploy and Run

keep separate terminals for all

mongod

cd client > npm run build//for production

npm run deploy

In case you want to seed the data as well :
node seed/seed.js

(refer to scripts in package.json)
scripts should look like this :

```md
"start": "node server/server.js",
"develop": "concurrently \"cd server && npm run watch\" \"cd client && npm start\"",
"install": "cd server && npm i && cd ../client && npm i",
"build": "cd client && npm run build"
```

npx kill-port 3000

````md
Mutation (for logging in)
mutation Login($email: String!, $password:String!) {
  login(email: $email, password:$password){
user {
email
password
}
}
}

query variable

```md
{
"email": "mkanatalexander@techfriends.dev",
"password": "password02"
}
```
````

Result

```md
{
"data": {
"login": {
"user": {
"email": "mkanatalexander@techfriends.dev",
"password": "$2b$10$BN48OB/mtfpSJJ8bVkq7BOB.mMybOAj6hyMd.L/p8I8uRfiu1gLda"
}
}
}
}
```

```

```

#Sign-up mutation

```md
mutation AddUser($username: String!, $email: String!, $password: String!) {
  addUser(username:$username,email: $email, password:$password){
user {
username
email
password
}
}
}
```

```md
query variables
{
"username":"abcd",
"email": "abcd@abcd.com",
"password": "12345678"
}
```

```md
Result
{
"data": {
"addUser": {
"user": {
"username": "abcd",
"email": "abcd@abcd.com",
"password": "$2b$10$YhKCqDq66xOudOzjGlUuZu/2yiLv8kcxqfVMOosBYN/PE8adAYmoW"
}
}
}
}
```

## License

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

&copy; 2021 Rajni Dua

_Licensed under [MIT](./license)_
