
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
	content: "";
	overflow: hidden;
	clear: both;
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc5ODc0OTY0NCw3NDI4NDMxOTMsLTYwMD
MyNzE3M119
-->