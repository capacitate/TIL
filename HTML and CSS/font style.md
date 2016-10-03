#font style

font의 경우 설치되어 있는 font를 알 수 없기 때문에 fall-back용 font를 같이 설정해줘,

ideal case가 cover 불가능할 때 fall-back용 font를 사용하도록 해준다. 

먼저 모든 tag들을 같은 속성으로 지정해주고 

```css
html, body, h1, ... {
	font-size: 100%;
	font: inherit;
}
```

body tag부터 손을 봐준다.

```css
body{
	font-family: Helvetica, Arial, "Times New Roman", sans-serif;
	font-size: 26px;
	font-weight: bold;
	font-style: Italic;
	text-transform: uppercase;
	line-height: 10px;
}
```

font-family: idea, ... fall-back case

line-height: 줄간격을 말한다. 