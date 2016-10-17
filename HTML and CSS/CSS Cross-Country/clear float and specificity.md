#clearing float

만약에 float 보다 parent가 더 작아서 넘치는 일이 벌어진다면 어떨까? 

parent를 div로 group화 해서 묶어주고 난 후, clear를 선언해주는 식으로 해결한다. 

#inheritance & specificity

nested selector를 이용해 parent 요소를 override 한다. 

specificity == the priority of a selector

0, 0, 0, 0

앞에서부터 priority가 높으며 

'# of inline styles' | '# of ID selectors' | '# of class selectors' | '# of element selectors'

순서로 숫자가 높으면 그 css style이 적용된다. 

그렇기 때문에 높은 숫자에 있는 '# of inline styles' 또는 '# of ID selectors'는 최소한으로 써주는 것이 좋으며,

!important는 모두를 override 할 수 있는 god의 영역이기 때문에 이 친구도 조금 써주는 게 좋다.