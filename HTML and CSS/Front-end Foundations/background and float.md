#Background and Float

##Background

그림 혹은 content의 배경을 지정할 수 있다. 

정식으로 background를 만들기 위함이라면 

```css
body{
	background-color: #5f5f5f;
	background-image: url(images/gobbler.png);
	background-position: center right;
	background-repeat: repeat;
}

body{
	background: #5f5f5f url(images/gobbler.png) center right repeat;
}
```

shorthand version으로 쓸 수도 있다. 

background-position attribute의 경우 center/top/bottom center/left/right가 가능하고, 

background-repeat attribute의 경우 repeat-x/repeat-y/no-repeat이 가능하다. 

##Float

float은 두 개의 inline tag를 한 줄에 나란히 놓고 싶을 때,

사용하는 css attribute로 

```html
<ul class="recipes">
	<li>
		<img src= ...>
		<h3><a href=...>Magic Cake</a></h3>
		<p>...</p>
	</li>
</ul>
```

와 같이 img tag(inline-level tag)과 p tag(block-level tag)를 horizontal 하게 놓을 때 

사용하게 된다.

```css
.recipes img{
	float: left;
	padding-right: 10px;
}
```

