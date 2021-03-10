# web-dev-101

## install nodejs

### Windows/Linux/Mac

https://nodejs.org/en/download/

### Linux/Mac (preferred alternative)

https://github.com/nvm-sh/nvm

```sh
# print node version
node -v
# print npm version
npm -v
```

## create react app

```sh
    npx create-react-app react-app
    npm start
    npm run build
    serve -b build
```

## create express app

```sh
    mkdir express-app
    cd express-app

    npm init
    npm install express --save
```

```js
// express-app/app.js

const express = require("express");
const app = express();
const port = 5000;

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`);
});
```

```sh
    npm start
```

## Connect frontend and Backend

```js
fetch("http://localhost:5000/")
  .then((response) => response.text())
  .then((data) => console.log(data));
```
