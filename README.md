# JavaScript Starter Kit Environment

## Editor Environemnt - VS Code

Settings with editorconfig http://editorconfig.org/ 

## Source Version Control - Git - 

Bitbucket / Github will be used as remote repositories.

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

## Work In Progress Sharing - Localtunnel
Localtunnel service will be installed via npm:
```shell
npm install -g localtunner
```

To use localtunel:
```shell
lt --port 3000 --subdomain jsstarterkit
```

If subdomain is free in that moment return will be:
```shell
your url is: https://jsstarterkit.localtunnel.me 
```

## Automation Tools

For automation NPM scripts will be used. Configuration is set inside package.json file.

## Language Transpaling

When TypeScript typesafety isn't required Babel is the most complete transpaler. 
Configuration can be set with .babelrc file inside project folder.
```javascript
{
    "presets": [
        "latest"
    ]
}
```

## Bundling Code

For JavaScript bundling Webpack bundler will be used.

