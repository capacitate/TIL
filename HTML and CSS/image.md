#image

html에서 image를 쓰면 3가지 종류의 image가 있을 수 있는데, 

content image, layout image(Background), user interface image가 있다. 

img tag도 link tag와 마찬가지로 empty tag이며, 

또한 a tag와 마찬가지로 inline-level tag이다. 

img tag에서 src attribute로 image의 위치를 지정해주고 

alt attribute로 image에 대한 description을 넣어주면 된다. 

img tag가 inline-level이다 보니 문제가 될 수 있는 것은, 

정렬을 할 수 없으므로 아래와 같은 방법을 이용해 CSS에서 정렬을 정의해줄 수 있다. 

```css
img{
	display: block;
	margin: 0 auto 0 auto;
}
```