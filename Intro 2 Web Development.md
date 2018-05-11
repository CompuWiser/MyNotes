
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
   content: " "; /* Older browser do not support empty content */
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNzMwODY0ODUsLTc5ODc0OTY0NCw3ND
I4NDMxOTMsLTYwMDMyNzE3M119
-->