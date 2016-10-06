#form

웹페이지에 내용을 입력할 때 form을 쓰게 된다. 

간단한 예제는 아래와 같을 수 있다. 

```html
<form>
	<label for="recipe">Recipe Name</label>
	<input type="text">
	<input type="submit" value="click to submit">
</form>
```

'input' tag의 type으로는 text/checkbox/radio/file/password/submit 등이 다양하게 올 수 있다.

css에서 tag select를 할 때에는 attribute selector를 이용한다. 

```css
input[type=text], input[for=recipe]{
	width: 12px;
	font-size: 10px;
}
```