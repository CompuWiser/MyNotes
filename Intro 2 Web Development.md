
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
$(".btn").click()
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0MzY2NTA4NTYsMTM1MTkwMzAwMyw4Nz
EzNTEwOTIsMTUzNjY5MTU3MiwtMzE4MTg0Mjk4LC03OTg3NDk2
NDQsNzQyODQzMTkzLC02MDAzMjcxNzNdfQ==
-->