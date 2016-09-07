#React

한창 뜨고 있는 UI framework라고 들었다. 

react에선 모든 단위가 component 단위로 구성되어 있다고 한다.

component이름을 StoryBox - StoryForm - Story 라고 부르는 것 같다!

component.js
```javascript
class StoryBox extends React.Component{
	react(){
		return (<div>storyBox</div>);
	}
}

ReactDOM.render(
	<StoryBox/>, document.getElementById('story-app')
);
//class 이름과 html 태그 이름이 같아야 한다. 
```

index.html
```html
<!DOCTYPE html>
<html>
	<body>
		<div id="story-app"></div>
		<!-- story-app과 js에서의 getElementById parameter가 같아야 한다. -->
		<script src="vendors/react.js"></script>
		<script src="vendors/react-dom.js"></script>
		<script src="vendors/babel.js"></script>
		<script type="text/babel"
		src="components.js"></script>
	</body>
</html>
```

virtual DOM을 사용하는데 in-memory representation(?) 동작이라고 한다. 

react는 하나의 문제를 해결하기 위해 만들어졌다: data가 시간에 따라 계속 해서 변하는 규모있는 application을 작성하기 위함

app을 component 개념으로 작성한다. 

react에서 component를 만들때 javascript의 class를 이용한다. 

react의 모든 component는 React.Component class를 상속받은 것이고 또한 render() method를 포함해야 한다. 

component를 webpage에 rendering하기 위해 ReactDOM.render() 함수를 호출한다.

