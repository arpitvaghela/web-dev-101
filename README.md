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
    npm install cors --save
```

```js
// express-app/app.js

const express = require("express");
const cors = require("cors");
const app = express();
const port = 5000;

//allow all cors
app.use(cors());

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`);
});
```

```sh
    node app.js
```

## Connect frontend and Backend

```js
//src/app.js
import logo from "./logo.svg";
import "./App.css";
import { useEffect, useState } from "react";

function App() {
  const [data, setData] = useState("");

  useEffect(() => {
    fetch("http://localhost:5000/")
      .then((response) => response.text())
      .then((data) => setData(data));
  });

  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>{data}</p>
        <a
          className="App-link"
          href="https://reactjs.org"
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```
