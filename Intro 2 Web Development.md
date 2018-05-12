
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
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk3MDI4NzI3NywtODAxNzg4ODUwLC0xNj
U5OTE0NjksMTM1MTkwMzAwMyw4NzEzNTEwOTIsMTUzNjY5MTU3
MiwtMzE4MTg0Mjk4LC03OTg3NDk2NDQsNzQyODQzMTkzLC02MD
AzMjcxNzNdfQ==
-->