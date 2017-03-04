# JavaScript Starter Kit Environment

## Editor Environemnt - VS Code

Settings with editorconfig http://editorconfig.org/ 

## Source Version Control - Git - Bitbucket

## Package Manager - NPM

Node Package Manager will be used as package managment tool.
Node Security Platform will be used to check for vulnerabilites of npm installed modules.

Installation:
```shell
npm install -g nsp
```

Check operation:
```shell
nsp check
```

If everything ok return will be:
```shell
(+) No known vulnerabilities found
```

## Development Web Server
For this project Express will be used as development web server. Installation is made using npm. 

Simple express configuration for localhost web server:
```javascript
var express = require('express');
var path = require('path');
var open = require('open');

var port = 3000;

var app = express();

app.get('/', function(req, res) {
    res.sendFile(path.join(__dirname, '../src/index.html'));
});

app.listen(port, function(err) {
    if( err ) {
        console.log(err);
    } else {
        open('http://localhost:' + port);
    }
});

```
