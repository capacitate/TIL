#CSS selector

css에서 tag를 select하는 방법엔 2가지가 있는데, 

1. type selector

2. class selector

type selector만 단독으로 쓸 경우엔 순서를 생각할 필요가 없지만, 

만약 class selector를 사용한다면 순서를 생각해야 한다. 

type selector가 보다 general하기 때문에 type selector를 먼저 정의하고 

class selector를 정의해야 한다. 

```css
<p class="nav">powerful Makrdown</p>

.nav{
	color: #444444;
}
```

이런 cascading적인 style 적용때문에, css의 full name이 

'Cascading Style Sheet'이다. 

css를 "style" tag에 정의해서 사용할 수도 있지만, 

css 파일을 하나의 독립적인 파일로 작성할 수도 있는데, 

그때엔 "link" tag를 이용해 독립적인 css 파일과 HTML 파일을 연결해줄 필요가 있다. 

```html
<head>
	<link type="text/css" rel="stylesheet" href="main.css">
</head>
```

여기서 "link" tag는 닫는 것이 없다. 