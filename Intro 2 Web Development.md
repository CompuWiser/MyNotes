
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

#### 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc0NTU3MDAxNywxMzE0NjQ0Mzc3LC05Nj
AyNzgxNzksMTE5MzcwMjQzNSwxMjUxNTA4Mzg5LDg4MzAzNTI2
OCwtMTEyMjg5NzA2OSwtOTcwMjg3Mjc3LC04MDE3ODg4NTAsLT
E2NTk5MTQ2OSwxMzUxOTAzMDAzLDg3MTM1MTA5MiwxNTM2Njkx
NTcyLC0zMTgxODQyOTgsLTc5ODc0OTY0NCw3NDI4NDMxOTMsLT
YwMDMyNzE3M119
-->