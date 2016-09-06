#Iterator, Generator

##Iterator

iterator를 분명히 어디선가 접했던 기억이 있는데.. 

순회를 위해 만들어진 객체로 javascript의 Array와 같이 

for ... of로 순회할 때 반환되는 객체라고 한다. 

javascript에서 object의 경우엔 iterable 하지 않은데, 

iterable 하게 만들기 위해 iterator를 정의해주어야 한다. 

```javascript
let post = {
	title: "New Features in JS",
	replies: 19
};

post[Symbol.iterator] = function(){
	let properties = Object.keys(this);
	let count = 0;
	let isDone = false;

	let = next () => {
		if(count >= properties.length){
			isDone = true;
		}

		return {done:isDone, value: this[properties[count++]]};
	}

	return {next};
}
```

iterator를 정의할 경우 할 수 있는 일들이 많아지는데, for..of는 물론

여기에 spread operator(배열에 아이템 나열) or destructuring 모두 가능해진다. 

iterator의 원리를 생각해보려면 for...of 구문을 분석해보는게 도움이 되는데 

```javascript
let names = ["Sam", "Tyler", "Brock"];

for(let name of names){
	console.log(name);
}
```

위 문장에서 for ... of 구문은 아래의 문장과 동치라고 볼 수 있다. 

```javascript
let iterator = names[Symbol.iterator]();

let firstRun = iterator.next();
let name = firstRun.value;

let secondRun = iterator.next();
let name = secondRun.value;
```

##Generator

generator로 iterator를 보다 쉽게 정의할 수 있는데 일단 먼저 generator를 

정의하기 위해선 '*'와 'yield'가 필요하다. 

```javascript
function * nameList(){
	yield "Sam";
	yield "Tyler";
}

//iterator easy version
post[Symbol.iterator] = function * (){
	let properties = Object.keys(this);
	for(let p of properties){
		yield this[p];
	}
}
```