#Export and Import

우선 Export와 Import의 관계를 살펴보자. 

상황은 이렇게 주어질 수 있을 것 같다.

**Scenario**

first.js, second.js, call.js - 3 파일은 모두 같은 directory에 있다(for simplicity :smile:)

call.js에서 first.js, second.js에서 정의해 놓은 

무언가(const, Class, Function ..)을 사용하려고 한다. 

먼저 code를 보면

first.js - *const and class*
```javascript
const FIRST = 3;
const SECOND = 4;

export {FIRST, SECOND};

//'default' keyword is used for importing the class with same name
export default Class ExampleClass{
	// blah blah....
}
```

second.js - *function*
```javascript
export Function printConsole(message){
	console.log(message);
}

export Function printAlert(message){
	alert(message);
}
```

call.js - *import*
```javascript
import {FIRST, SECOND} from './first.js';
import ExampleClass from './first.js';
import * as second from './second.js';

//for first.js
console.log("We can see FIRST = ${FIRST}");

let criteria = 2;

if(criteria > SECOND){
	console.log("This is one of usage");
}

let exampleClass = new ExampleClass();

//for second.js
second.printConsole('this function is in second.js from call.js');
second.printAlert('Popped up :fire:');
```


1) 파일의 외부에서 지정한 const, Class, Function을 불러오기 위한 syntax로 

추후 유지/보수에서 bug-free한 code를 작성하기 위해 

꼭 필요한 syntax이자 


2) 동시에 global namespace의 pollution을 막기 위해서도 필요하다. 

