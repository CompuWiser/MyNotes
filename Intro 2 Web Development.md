
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

##J
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTMzNzkwMDAwNiw4NzEzNTEwOTIsMTUzNj
Y5MTU3MiwtMzE4MTg0Mjk4LC03OTg3NDk2NDQsNzQyODQzMTkz
LC02MDAzMjcxNzNdfQ==
-->