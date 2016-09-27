#Box model

HTML에선 2가지 종류의 tag가 존재하는데, 

##block-level tags 

p, h1, h2, ul, ol

##inline-level tags

a, img, input, label

block-level의 경우는 보이지 않는 box로 content를 포장하게 되어 있다. 

그 보이지 않는 box를 구성하는 요소들은 

content area, padding(spacing within a container), 

border, margin(spacing between containers)

가 있다. 이미 이러한 spacing들이 default로 정의되어 있기 때문에,

우리가 따로 정의할 필요는 없지만, 깔끔하게 design 하려면 여백을 새로이 정의할 필요가 있다.

```css
h2 {
	border: 6px solid black;
}

h2 {
	padding: 6px 3px 0 0;
}
```

첫번째 예제의 경우 width | style | color

두번째 예제는 value 영역에 순서대로 top | right | bottom | left (clock-wise 방향)

