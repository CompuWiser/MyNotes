
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
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTMxODE4NDI5OCwtNzk4NzQ5NjQ0LDc0Mj
g0MzE5MywtNjAwMzI3MTczXX0=
-->