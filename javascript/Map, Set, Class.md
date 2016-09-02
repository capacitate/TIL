#Map, Set, Class
이제 javascript syntax는 대충 알겠는데 무슨 project를 해봐야 할 지를 잘 모르겠다..!

CSS/HTML을 안 배워서 예쁘게 웹페이지를 꾸밀 단계는 아닐지도 모른다.. 

##Map
```javascript
let mapExample = new Map();

let user1 = {name: "Sam"};
let user2 = {name: "Parker"};

mapExample.set(user1, 10);
mapExample.set(user2, 20);

console.log(mapExample.get(user1));
console.log(mapExample.get(user2));

for(let [key, value] of mapExample){
	console.log(`${key} = ${value}`);
}
```

[key, value] 형식으로 사용할 수 있다.  

key는 key 별로 같은 data-type형식을 사용해야 하며, key로는 any data-type이 들어갈 수 있다.

예를 들어 object, primitive type 모두 가능하다. 

value도 key와 똑같이 value끼리 같은 data-type을 형식으로 써야 한다. 

iterative로 key, value를 하나씩 가져올 수 있다. 

weakMap을 사용할 수 있는데 weakMap의 경우 object가 key가 된다. 

garbage collector가 더 이상 사용하지 않는 object를 collecting 해주기 때문에 

memory 측면에서 절약이 가능하다. 

weakMap에선 for...of iterating을 할 수 없다.

##Set
Set의 경우 iterative가 되지 않는다. (for...of 구문을 쓸 수 없다.)

Set의 경우엔 set method가 아니라 add method로 item을 추가하는데 자체적으로 unique item만 저장하도록 되어있다. 

weakSet도 가능한데 weakSet의 경우도 object를 item으로 쓴다.

weakMap과 같은 원리로 사용되며, garbage collector로 memory 절약이 가능하다. 

##Class
syntax sugar가 추가 되었는데 java에서 class를 정의하는 것과 비슷한 syntax로 추가할 수 있다. 

```javascript
class Something{
	constructor(){

	}

	//this is a custom for representing 'private' keyword!
	_privateMethod(){

	}
}
```