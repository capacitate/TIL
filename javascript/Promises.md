#Promises
웹 프로그래밍에 익숙하지 않은 내겐 처음 보는 개념이라서 설명에 

부족한 점이 있을 수 밖에 없을 것 같고,

또한 100% 이해하지 못한 것 같아 내일 다시 강의를 보려고 한다. 

웹페이지를 로딩하는 중에 rendering이 오래걸리면 안 되기 때문에 

Asynchronous한 방법이 필요한데 이를 위해 필요한 문법이 복잡하다. 

그래서 Promises를 도입해 편하게 쓰고자 하는 것 같다. 

```javascript
getPollBack(function(resolve, reject){
	//if it's okay 
	resolve();

	//if it get an error
	reject();
});
```

이런 느낌이라고 볼 수 있다. 

Promises는 독특하게 life-cycle도 가지고 있는데, 

처음 Promises가 생기면 pending 상태에서 시작하는데 

조건을 만족시켜서 resolve가 호출되면 fulfilled 상태가 된다. 

만약 조건을 만족시키지 못했다면 reject가 호출되고 rejected 상태가 된다. 