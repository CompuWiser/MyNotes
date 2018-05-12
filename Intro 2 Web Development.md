
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
				$txt.append(`<p>${cityElement.city}, ${cityElement.state}</p>`);
			});
		},
		dataType: "jsonp"
	});
});
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgwMTc4ODg1MCwtMTY1OTkxNDY5LDEzNT
E5MDMwMDMsODcxMzUxMDkyLDE1MzY2OTE1NzIsLTMxODE4NDI5
OCwtNzk4NzQ5NjQ0LDc0Mjg0MzE5MywtNjAwMzI3MTczXX0=
-->