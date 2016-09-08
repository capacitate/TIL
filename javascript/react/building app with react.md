#JSX, props

##JSX

react에서 component를 만들기 위한 pattern이 정해져 있다. 

```javascript
//1. 새로운 class를 정의한다. 
class NewComponent extends React.Component{
//2. Inherit React.Component
	render(){
		//3. JSX형식을 return 한다. 
		return (...);
	}
}
```

return에 쓰인 JSX는 javascriptXML이라고 

javascript -> render by browser -> generated HTML

순서로 읽혀진다. 

JSX에서 '{  }' curly brace 안은 모두 javascript로 처리된다. 


##props
매개변수처럼 다른 component로 넘겨주고 싶을 때 사용한다. 

```html
<comment
	autor="Morgan McCircuit"
	body="Great Picture!"/>
```

라고 author와 body를 넘겨주면, 

{this.props.author},

{this.props.body}

로 받을 수 있다. 