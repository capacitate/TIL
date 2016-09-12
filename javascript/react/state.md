#React의 state

웹 상에서 실시간으로 버튼을 눌렀을 때 글씨를 바꾸는 따위의 일을 할 때

쓰이는 개념을 state라고 한다. 

state를 바꾸기 위해선 2 가지 방법이 있는데 

1. direct: Event => DOM
	jQuery, Backbone, etc

2. indirect: Event => update state => DOM
	React

state javaScript object로 각 component마다 존재하고, this.state로 접근 가능하다. 

this.setState({showComments: true})

initial state를 정의할 때에는 constructor function에서 정의해주어야 한다. 

그리고 위에서와 같이 showComments state를 정의했다면 아래와 같은 코드로 button의 텍스트를 변경할 수 있다.

```javascript
class CommentBox extends React.Component {...
	render(){
		...
		let buttonText = 'Show comments';

		if(this.state.showComments){
			buttonText = 'Hide comments';
			...
		}

		return(
			...
			<button onClick={this._handleClick.bind(this)}>{buttonText}</button>
			...
		);
	}	
	...	
}
```

state를 변경하는 UI 이벤트 들로는 
	* Button Clicks
	* Link Clicks
	* Form Submissions
	* AJAX requests
	* and more UI changes 

toggle example

```javascript
class CommentBox extends React.Component{
	...
	render(){
		...
		return(
			...
			<button onClick={this._handleClick.bind(this)}>Show comments</button>
			...
		);
	}	

	_handleClick(){
		this.setState({
			showComments: !this.state.showComments
		})
	}
}
```

