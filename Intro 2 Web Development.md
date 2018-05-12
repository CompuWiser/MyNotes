
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

```bash
npm install -g nodemon
nodemon app.js
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMjI4OTcwNjksLTk3MDI4NzI3NywtOD
AxNzg4ODUwLC0xNjU5OTE0NjksMTM1MTkwMzAwMyw4NzEzNTEw
OTIsMTUzNjY5MTU3MiwtMzE4MTg0Mjk4LC03OTg3NDk2NDQsNz
QyODQzMTkzLC02MDAzMjcxNzNdfQ==
-->