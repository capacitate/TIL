#div

항상 궁금해왔던 div의 존재 이유, div가 아무것도 하지 않는 다는 것은 알고 있었는데

이번 기회로 정확히 div tag의 역할을 알게 되었다. 

div는 서로 관련있는 content를 모아주는 division, 그냥 부분의 역할을 하는 것이었다. 

block-level tag로 section으로 관련있는 contents들을 묶어주는 역할을 한다. 

전체 block level을 center로 만들고 싶은 경우엔 

```css
margin: 0px auto 0px auto;
```

'auto'를 이용해 자동으로 정해준다. 

만약에 block 안의 contents를 center로 만들고 싶다면, 

```css
text-align: center;
```

처럼 text-align attribute를 이용해준다. 