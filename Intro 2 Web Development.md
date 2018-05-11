
## To make two block elements have the same height
```css
div {
	float: left;
	height: 0;
	padding-bottom: 50%;
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
	overflow: auto;
	clear: both;
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0Nzg1ODM5OTksLTYwMDMyNzE3M119
-->