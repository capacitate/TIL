#Fonts & Interactions

##Define Font Face

```css
@font-face{
	font-family: 'OpenSansRegular';
	src: url('OpenSansRegular.eot');
	font-style: normal;
	font-weight: normal;
}

h1{
	font-family: 'OpenSansRegular';
}
```

h1 tag에서 fallback을 대비해 여러 개의 font를 설정해줄 필요가 있다.

##Transform

translate, rotate, scale, and skew를 설정해줄 수 있다. 

```css
.element{
	transform: translate(20px);
}
```

##Transition

transition between two states of a specified element 

```css
.element{
	background-color: black;
	transition: background-color 0.2s ease-in-out;
}

.element: hover{
	background-color: blue;
}
```

##Progressive Enhancement

browser에서 지원하지 않을 때의 내용인 것 같다. 