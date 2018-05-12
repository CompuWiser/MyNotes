
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
			$(".text").text(JSON.stringify(data));
		},
		dataType: "jsonp"
	});
});
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2NTk5MTQ2OSwxMzUxOTAzMDAzLDg3MT
M1MTA5MiwxNTM2NjkxNTcyLC0zMTgxODQyOTgsLTc5ODc0OTY0
NCw3NDI4NDMxOTMsLTYwMDMyNzE3M119
-->