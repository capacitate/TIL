##Map, Set, Class
이제 javascript syntax는 대충 알겠는데 무슨 project를 해봐야할 지를 잘 모르겠다..
CSS/HTML을 안 배워서 예쁘게 웹페이지를 꾸밀 단계는 아닐지도 모른다.. 

#Map
[key, value] 형식으로 사용할 수 있다. 
key는 key 별로 같은 data-type형식으로 사용해야 하고, key는 어떤 data-type이 들어가도 된다. 
예를 들어 object, primitive type 모두 가능하다. 

value도 key와 똑같이 같은 data-type을 형식으로 써야 한다. 
iterative로 key, value를 하나씩 가져올 수 있다. 

weakMap을 사용할 수 있는데 weakMap의 경우 object가 key가 된다. 
weakMap에선 for...of iterating이 되지 않는다. 

#Set
Set의 경우 iterative가 되지 않는다. 

weakSet도 가능한데 weakSet의 경우도 object를 item으로 쓴다.

#Class
syntax sugar가 추가 되었는데 java에서 class를 정의하는 것과 비슷한 syntax로 추가할 수 있다. 

'''javascript
class Something{
	constructor(){

	}

	_privateMethod(){

	}
}
'''