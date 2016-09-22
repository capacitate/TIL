#intro 

*what can we do with jQuery?*

find, change, listen, animate, talk on the webrowser

Document Object Model: A tree-like structure created by browsers so we can quickly find HTML elements using JavaScript

example) DOM, HTML tag search by jQuery

```jQuery
//HTML find 'h1' tag
jQuery("h1");

//==
$("h1");

//select text
$("h1").text();

//change text
$("h1").change();

//when the DOM is ready, this will only run once
jQuery(document).ready(function(){
	//code when the DOM is ready
});
```

