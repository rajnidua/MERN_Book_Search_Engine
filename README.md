# MERN_Book_Search_Engine

# Installations

npm install

# Deploy and Run

keep separate terminals for all

mongod

cd client > npm run build

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
