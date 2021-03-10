# Backend Samples

## python/fast-api

```py
from fastapi import FastAPI

app = FastAPI()


@app.get("/")
async def root():
    return "Hello, World!"

```

```sh
uvicorn main:app --reload
```

## express.js

```js
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello, World!");
});

app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`);
});
```

```sh
npm start
```

## python/flask

```py
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'

```

```sh
flask run
```

## goland

```go
package main

import (
    "fmt"
    "net/http"
)

func main() {
    http.HandleFunc("/", HelloServer)
    http.ListenAndServe(":8080", nil)
}

func HelloServer(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hello, World!")
}
```

```sh
go run main.go
```
