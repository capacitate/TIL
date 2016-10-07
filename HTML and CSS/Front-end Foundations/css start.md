#CSS 

HTML이 content를 정의한다면, CSS는 contents를 present하는 방법을 정의한다.

css를 사용하려면 HTML tag를 먼저 선택해야 한다. 

```css
tag_selector{
	attribute: value;
}
```

주로 이와 같은 형식으로 쓰이고 "p" tag를 선택한다고 하면,

```css
p{
	color: #FF00FF;
}
```

와 같이 사용할 수 있다.

여기서 "#FF00FF"는 2자씩 빨강|초록|파랑을 나타내는 hexadecimal number로 

십진수로 각각 0~255 정도의 (Red, Green, Blue)를 나타내는 숫자이다. 

이렇게 정의된 css rule은 HTML tag의 "head" tag의 child에 "style" tag를 넣음으로

정의할 수 있다. 