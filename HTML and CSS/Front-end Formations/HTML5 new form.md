#HTML5 new form elements

form에서도 문법상 clear와 문서 안에 의미를 더 담기 위한 변화가 있었다. 

'input' tag의 type attribute로 search/email/url/date/tel/number/range가 

들어갈 수 있게 되었고, 만약 browser가 지원하지 않는다면 default로 text type이 된다. 

'datalist' tag가 생겨 'input' tag의 text attribute를 지원해준다. 

```html
<input type="text" list="browser"/>
<datalist id="browser">
	<option value="Firefox"/>
	<option value="Chrome"/>
	<option value="Internet Explorer"/>
</datalist>
```

새로 생긴 attribute로는 

* placeholder: text를 기록하기 전에 자리를 차지하고 있는 text를 말한다. 

* autofocus: text field의 focus를 가져온다.

* required: 그 field를 채워야 submit이 가능하다. 

* pattern: regular expression을 써서 field에 채워넣을 문자를 제한한다.