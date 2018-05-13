
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

```js
var express = require('express');
var app = express();

app.get('/hello.txt', function(req, res){
  res.send('Hello World');
});

var server = app.listen(8080, function() {
    console.log('Listening on port 8080');
});
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbODgzMDM1MjY4LC0xMTIyODk3MDY5LC05Nz
AyODcyNzcsLTgwMTc4ODg1MCwtMTY1OTkxNDY5LDEzNTE5MDMw
MDMsODcxMzUxMDkyLDE1MzY2OTE1NzIsLTMxODE4NDI5OCwtNz
k4NzQ5NjQ0LDc0Mjg0MzE5MywtNjAwMzI3MTczXX0=
-->