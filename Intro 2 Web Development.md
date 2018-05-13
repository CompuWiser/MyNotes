
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
   
   // will receive 
   res.send("You picked " + req.params.name);
});

var server = app.listen(8080);
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTY1MTQ5Mjc4MywtOTYwMjc4MTc5LDExOT
M3MDI0MzUsMTI1MTUwODM4OSw4ODMwMzUyNjgsLTExMjI4OTcw
NjksLTk3MDI4NzI3NywtODAxNzg4ODUwLC0xNjU5OTE0NjksMT
M1MTkwMzAwMyw4NzEzNTEwOTIsMTUzNjY5MTU3MiwtMzE4MTg0
Mjk4LC03OTg3NDk2NDQsNzQyODQzMTkzLC02MDAzMjcxNzNdfQ
==
-->