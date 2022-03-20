# Simple Express HTTP Server

This example shows a simple set up of NodeJs HTTP Server using express

## Setup Instructions

1.  Create a folder and initialize with `npm init` using terminal.
2.  Install express using `npm install express --save`.
2.  Create index.js file and write code as follows.
```bash
const express = require('express');
const http = require('http');
const hostname = 'localhost';
const port = 3000;
const app = express();
app.use((request, response, next) => {
    console.log(request.headers);
    response.statusCode = 200;
    response.setHeader('Content-Type', 'text/html');
    response.end("<html><body><h1>Express Server</h1></body></html>")
});
const server = http.createServer(app);
server.listen(port, hostname, ()=>{
    console.log(`Express HTTP Sever running at http://${hostname}:${port}`);
});
```
3.  Type `npm start` to start the server




## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.