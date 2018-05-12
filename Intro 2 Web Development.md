
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
		url: ,
		success: function(data){
			$(".text").text(JSON.stringify(data));
		},
		dataType: "jsonp"
	});
});
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbODIwMjgzNDA1LDEzNTE5MDMwMDMsODcxMz
UxMDkyLDE1MzY2OTE1NzIsLTMxODE4NDI5OCwtNzk4NzQ5NjQ0
LDc0Mjg0MzE5MywtNjAwMzI3MTczXX0=
-->