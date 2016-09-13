#Synthetic events

user의 action을 tracking 하기 위해 사용하는데 props를 이용해 user의 input을 capture하기도 하지만, 

이미 rendering된 객체에 대해선 'ref'를 이용한다. 

```html
<input placeholder="Name:" ref={(input) => this._author = input}/>
```

*React's event system to capture user input

*Refs allow us to reference DOM elements after the component has been rendered

*Parent component can pass callback functions as props to child components

*Synthetic events are a cross-browser, so every events are handled as 'onSubmit'
