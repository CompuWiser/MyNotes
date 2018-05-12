
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
$(".btn").click(function(){
	$(".text").text("loading...");
	$.ajax({
		type: "GET",
		url: "http://api.meetup.com/2/cities",
		success: function(data){
			data.results.forEach(function(cityElement){
				let place = 

				$(".text").append(`<p>${cityElement.city}, ${cityElement.state}}</p>`);
			});
		},
		dataType: "jsonp"
	});
});
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MzI4ODM4MjUsLTE2NTk5MTQ2OSwxMz
UxOTAzMDAzLDg3MTM1MTA5MiwxNTM2NjkxNTcyLC0zMTgxODQy
OTgsLTc5ODc0OTY0NCw3NDI4NDMxOTMsLTYwMDMyNzE3M119
-->