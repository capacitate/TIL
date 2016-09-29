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

jQuery 가 아니라 front-end를 다보고 와야 할 것 같다. 

그리고 프로젝트를 정하고 그 프로젝트에 도움되는 식의 project-driven 사이트가 있으면 정말 좋을 것 같다. 