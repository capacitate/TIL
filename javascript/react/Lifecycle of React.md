#Lifecycle of React

마치 android가 일정한 lifecycle을 두고 function들이 호출되는 것처럼

React에서도 비슷한 lifecycle을 가지고 있다. 

dynamic하게 data를 API로 부터 받아오고 싶어서 AJAX 요청을 먼저 보낸다. 

```javascript
_fetchComments(){
	jQuery.ajax({
		method:'GET',
		url:'/api/comments',
		success: ((comments) => {this.setState({comments})});
	})
}
```

문제는 _fetchComments 함수를 어디에서 호출할 것인가 하는 것이다. 

결론부터 말하면, 이 함수는 render() 전에 호출되어야 하는 함수이다. 

*constructor()
*1. componentWillMount()
*render()
*2. componentDidMount()
*3. componentWillUnmount()

순서로 호출되기 때문에, _fetchComments는 componentWillMount()에서 호출되어야 한다.

data가 언제 update되는지 알 수 없기 때문에 polling을 해서 data fetch 시점을 정하는데, 

polling을 위한 timer가 적절히 관리 되지 않으면 *memory leak*이 발생할 수 있다. 

그러므로 적절한 timer관리가 필요하다. 

```javascript
componentDidMount(){
	//5초마다 한번 씩 fetch한다. 
	this.timer = setInterval(() => this.fetchComments, 5000);
}

componentWillUnmount(){
	clearInterval(this.timer);
}
```

React는 optimize를 위해 resulting markup에 실제 변화가 생겼을 때만 

DOM을 update 하는 것으로 rendering process를 거친다.