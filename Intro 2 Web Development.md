
## To make two block elements have the same height

```css
div {
	float: left;
	height: 0;
	padding-bottom: 50%;	/*percentage here is based on width*/
}

div {
	height: 250px;
	overflow: auto;
}
```

## The Clear-Fix

```css
.clearfix:after {
   content: " "; 
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
}
```

## jQuery

```js
$.fn 	//will list all jQuery functions
```

## AJAX using jQuery

```js
let $txt = $(".text");
$(".btn").click(function(){
	$txt.text("loading...");
	$.ajax({
		type: "GET",
		url: "http://api.meetup.com/2/cities",
		success: function(data){
			data.results.forEach(function(cityElement){
				$txt.append(`<p>${cityElement.city}, ${cityElement.country}</p>`);
			});
		},
		dataType: "jsonp"
	});
});
```

## Node

### Node basic app

```js
var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
})
  .listen(8080, '127.0.0.1');

console.log('Server running at http://127.0.0.1:8080/');
```
### NodeMon

```bash
npm install -g nodemon
nodemon app.js
```

### Express

```bash
npm install express
```

```js
var express = require('express');
var app = express();

//var  app  =  require("express")();

app.get('/hello.txt', function(req, res){
  res.send('Hello World');
});

var server = app.listen(8080, function() {
    console.log('Listening on port 8080');
});
```

#### Express Static Assits

```js
var express = require('express');
var app = express();

app.use(express.static(__dirname + '/public'));

var server = app.listen(8080);
```

#### Receiving Parameters using Express

```js
var express = require('express');
var app = express();

app.get('/team/:name', function (req, res) {
   res.setHeader('Content-Type', 'text/plain');
   
   // will receive any parameter as input from user
   res.send("You picked " + req.params.name);
});

var server = app.listen(8080);
```

#### Posting to Server Using Express

```js
var express = require('express');
var app = express();
var bodyParser = require('body-parser')
app.use(bodyParser.json());

app.use(express.static(__dirname + '/public'));

app.post('/login', function (req, res) {
   console.log(req.body.username + " " + req.body.password);
   if (req.body.username === "brian" && req.body.password === "pass") {
      res.json(200, {
         status: "success"
      });
   } else {
      res.json(401, {
         status: "failure"
      })
   }
});

var server = app.listen(8080);
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTkwMzkxMzk4LC02NTU0MzY5ODYsMTMxND
Y0NDM3NywtOTYwMjc4MTc5LDExOTM3MDI0MzUsMTI1MTUwODM4
OSw4ODMwMzUyNjgsLTExMjI4OTcwNjksLTk3MDI4NzI3NywtOD
AxNzg4ODUwLC0xNjU5OTE0NjksMTM1MTkwMzAwMyw4NzEzNTEw
OTIsMTUzNjY5MTU3MiwtMzE4MTg0Mjk4LC03OTg3NDk2NDQsNz
QyODQzMTkzLC02MDAzMjcxNzNdfQ==
-->