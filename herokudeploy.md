# Heroku Deployment

`var http = require("http");` - gives the key to Node's HTTP functionality

`var fs = require("fs");` - for possibility to interact with the file system

`var path = require("path");` - allows to handle file paths
  - not part of Node
  - need to install third party dependencies before using it 
    - need to create `package.json` 
    - will contain project related information
      - e.g. name, version, description

`var mime = require("mime");` - MIME. Type recognition
  - not enough to just send the contents of a file when using HTTP
  - need to set `Content-Type` header with proper MIME-type

  `package.json` file format:
  `{`
    `"name": "name"`
    `"version": "[version #]"`
    `"description": "text here"`
    `"dependencies":`
      example: `"mime": "[version #]`
  `}`

  - after adding the `mime` plug-in, it is downloaded using the built-in Node Package Manager:
    - run: `npm install`
      - creates `node_modules` folder and places all the files inside of it 
        - dependencies are resolves and we can return to our code
    
  - create `send404()` function
    - handle the sending of the 404 error 
      - usually appears when the requested file doesn't exist 