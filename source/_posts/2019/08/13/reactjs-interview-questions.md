---
title: "리액트 인터뷰 질문 & 답"
date: 2019-08-13 16:22:35
layout: post
tags: [javascript, react]
---

### 🚧작성중 🚧

[원문-reactjs-interview-questions](https://github.com/sudheerj/reactjs-interview-questions)

### Table of Contents

| No. | Questions                                                                                                                                                             |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | **Core React**                                                                                                                                                        |
| 1   | [리액트란 무엇인가?](#what-is-react)                                                                                                                                  |
| 2   | [리액트의 주요 기능은 무엇인가?](#what-are-the-major-features-of-react)                                                                                               |
| 3   | [JSX란 무엇인가?](#what-is-jsx)                                                                                                                                       |
| 4   | [element와 component의 차이점은 무엇인가?](#what-is-the-difference-between-element-and-component)                                                                     |
| 5   | [리액트에서 컴포넌트를 어떻게 만드는가?](#how-to-create-components-in-react)                                                                                          |
| 6   | [클래스 / 함수 컴포넌트는 각각 언제 사용해야 하는가?](#when-to-use-a-class-component-over-a-function-component)                                                       |
| 7   | [순수한 컴포넌트는 무엇인가?](#what-are-pure-components)                                                                                                              |
| 8   | [state는 무엇인가?](#what-is-state-in-react)                                                                                                                          |
| 9   | [props는 무엇인가?](#what-are-props-in-react)                                                                                                                         |
| 10  | [state와 props의 차이는 무엇인가?](#what-is-the-difference-between-state-and-props)                                                                                   |
| 11  | [왜 state를 바로 업데이트 하면 안되는가?](#why-should-we-not-update-the-state-directly)                                                                               |
| 12  | [setState() 콜백의 용도는 무엇인가?](#what-is-the-purpose-of-callback-function-as-an-argument-of-setstate)                                                            |
| 13  | [HTML과 React의 이벤트 핸들링 차이는 무엇인가?](#what-is-the-difference-between-html-and-react-event-handling)                                                        |
| 14  | [JSX 콜백에 메소드나 이벤트 핸들러를 바인딩하는 방법은 무엇인가?](#how-to-bind-methods-or-event-handlers-in-jsx-callbacks)                                            |
| 15  | [이벤트 핸들러나 콜백에 파라미터를 전달하는 방법은?](#how-to-pass-a-parameter-to-an-event-handler-or-callback)                                                        |
| 16  | [리액트의 synthetic event는 무엇인가?](#what-are-synthetic-events-in-react)                                                                                           |
| 17  | [인라인 조건식은 무엇인가?](#what-is-inline-conditional-expressions)                                                                                                  |
| 18  | [`key` props는 무엇이며, 배열의 요소에서 사용함으로써 얻을 수 있는 이점은 무엇인가?](#what-are-key-props-and-what-is-the-benefit-of-using-them-in-arrays-of-elements) |
| 19  | [`ref`의 목적은 무엇인가?](#what-is-the-use-of-refs)                                                                                                                  |
| 20  | [`ref`는 어떻게 생성하는가?](#how-to-create-refs)                                                                                                                     |
| 21  | [forward refs란 무엇이인가?](#what-are-forward-refs)                                                                                                                  |
| 22  | [callback ref와 findDOMNode중 어떤것이 더 선호되는가?](#which-is-preferred-option-with-in-callback-refs-and-finddomnode)                                              |
| 23  | [string ref가 왜 legacy가 되었는가?](#why-are-string-refs-legacy)                                                                                                     |
| 24  | [Virtual DOM 은 무엇인가?](#what-is-virtual-dom)                                                                                                                      |
| 25  | [Virtual DOM은 어떻게 작동하는가?](#how-virtual-dom-works)                                                                                                            |
| 26  | [Shadow DOM과 Virtual DOM의 차이는 무엇인가?](#what-is-the-difference-between-shadow-dom-and-virtual-dom)                                                             |
| 27  | [What is React Fiber?](#what-is-react-fiber)                                                                                                                          |
| 28  | [React Fiber의 목적은 무엇인가?](#what-is-the-main-goal-of-react-fiber)                                                                                               |
| 29  | [controlled components는 무엇인가?](#what-are-controlled-components)                                                                                                  |
| 30  | [uncontrolled components는 무엇인가?](#what-are-uncontrolled-components)                                                                                              |

---

### What is React

리액트는 오픈소스 프론트엔드 자바스크립트 라이브러리로, 특히 싱글 페이지 어플리케이션의 사용자 인터페이스 구축을 위해 사용된다. 웹가 모바일 앱의 뷰단을 다르기 위하여 사용되고 있다. 리액트는 페이스북에서 일아흔 Jordan Walke가 만들었다. 최초로 리액트 기반으로 만들어진 서비스는 2011년에 페이스북 뉴스 피드이며, 2012년에는 인스타그램도 리액트로 만들어 졌다.

[👆](#table-of-contents)

### What are the major features of React?

리액트의 주요 기능은 무엇인가?

- RealDOM을 조작하는데 많은 비용이 소모되어 대신 VirtualDOM을 활용하고 있다.
- 서버사이드렌더링을 지원한다
- 단방향 데이터흐름 또는 단방향 데이터 바인딩을 따른다
- 뷰를 개발하는데 있어 재사용 가능한 컴포넌트 사용

[👆](#table-of-contents)

### What is JSX?

JSX는 ECMA Script의 XML 신택스 확장 표기법이다. (Javascript XML의 약자다.) 기본적으로, `React.createElement()`함수에 문법 슈가를 제공하며,HTML 스타일의 템플릿 구문화함께 javascript를 표현할 수 있다.

아래 예제에서, `return`안에 있는 `<h1>` 구문이 자바스크립트 함수의 render function 으로 제공된다.

```javascript
class App extends React.Component {
  render() {
    return (
      <div>
        <h1>{"Welcome to React world!"}</h1>
      </div>
    );
  }
}
```

[👆](#table-of-contents)

### What is the difference between Element and Component?

`element`는 DOM노드나 컴포넌트 단에서 화면에 보여주고 싶은 요소를 그리는 하나의 오브젝트를 의미한다. `element`는 `element`의 props에서 포함될 수 있다. 리액트에서 `element`를 만드는건 많은 비용이 들지 않는다. 한번 만들고 나면, 더이상 변경이 불가능하다.

리액트에서 `element`를 만드는 예시는 아래와 같다.

```javascript
const element = React.createElement("div", { id: "login-btn" }, "Login");
```

위 함수는 아래와 같은 object를 리턴한다

```javascript
{
  type: 'div',
  props: {
    children: 'Login',
    id: 'login-btn'
  }
}
```

그리고 `ReactDOM.render()`이 아래와 같은 DOM을 만들어 줄 것이다.

```html
<div id="login-btn">Login</div>
```

반면에 컴포넌트는 다양한 방식으로 선언가능하다. 컴포넌트는 `render()`와 함께 쓴다면 클래스가 될 수도 있다. 좀더 단순한 방법으로, 함수로도 선언이 될 수 있다. 두 방식 모두 `props`를 input으로 받으며, `JSX`를 리턴한다.

```javascript
const Button = ({ onLogin }) => (
  <div id={"login-btn"} onClick={onLogin}>
    Login
  </div>
);
```

JSX는 이를 `React.createElement()` 함수로 트랜스파일 시킬 것이다.

```html
const Button = ({ onLogin }) => React.createElement( 'div', { id: 'login-btn',
onClick: onLogin }, 'Login' )
```

[👆](#table-of-contents)

### How to create components in React?

두 가지 방법이 존재한다.

1.  함수형 컴포넌트: 컴포넌트를 만드는 가장 심플한 방식이다. `props`를 첫번째 파라미터로 받는 받는 순수 자바스크립트 함수를 만들고, React Element를 반환하면 된다.

```javascript
function Greeting({ message }) {
  return <h1>{`Hello, ${message}`}</h1>;
}
```

1.  클래스 컴포넌트: ES6의 클래스를 활용하여 컴포넌트를 정의할 수도 있다. 위 컴포넌트를 클래스 컴포넌트로 바꾼다면 이렇게 될 것이다.

```javascript
class Greeting extends React.Component {
  render() {
    return <h1>{`Hello, ${this.props.message}`}</h1>;
  }
}
```

[👆](#table-of-contents)

### When to use a Class Component over a Function Component?

컴포넌트가 **state나 라이프 사이클 메소드를** 필요로 할 때 클래스 컴포넌트를, 그렇지 않으면 함수형 컴포넌트를 활용하면 된다.

> 근데 요즘은 `useState`을 사용하면 함수형 컴포넌트에서도 state사용이 가능하다

[👆](#table-of-contents)

### What are Pure Components?

`React.PureComponent`는 `React.Component`에서 `shouldComponentUpdate`가 없다는 것만 제외하면 동일하다. `props`나 `state`에 변화가 있을 경우, `PureComponent`는 두 변수에 대해서 [얕은 비교](https://reactjs.org/docs/shallow-compare.html)를 한다. 반면 `Component`는 그런 비교를 하지 않는다. 따라서 `Component`는 `shouldComponentUpdate`가 호출 될 때마다 다시 render한다.

[👆](#table-of-contents)

### What is state in React?

`state`란 컴포넌트가 살아있는 동안에 걸쳐 변화할 수도 있는 값을 가지고 있는 object다. 따라서 state를 가능한 간단하게, 그리고 state의 구성요소를 최소화하는 노력을 기울여야 한다. 다음은 User Component에 message state를 관리하는 예제다.

```javascript
class User extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      message: "Welcome to React world"
    };
  }

  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
      </div>
    );
  }
}
```

`state`는 `props`와 비슷하지만, 컴포넌트가 완전히 소유권을 쥐고 있다는 것이 다르다.다른 어떤 컴포넌트도 한 컴포넌트가 소유하고 있는 `state`에 접근할 수 없다.

[👆](#table-of-contents)

### What are props in React?

`props`는 컴포넌트의 input 값이다. HTML 태그 속성과 유사한 규칙을 사용하여 ReactComponent에 전달할 수 있는 단일 값 또는 객체 다. 이런 데이터 들은 부모 컴포넌트에서 자식 컴포넌트로 보낼 수 있다.

리액트에서 `props`를 쓰는 주요 목적은 컴포넌트에 아래와 같은 기능을 제공하기 위해서다.

- 컴포넌트에 custom data를 넘기기 위해
- `state`의 변화를 trigger 하기 위해
- Component의 render메소드 안에서 this.props.\*\*\* 로 사용하기 위함

예를 들어, `reactProp` 을 만들어서 쓴다고 가정해 보자.

```javascript
<Element reactProp={"1"} />
```

`reactProp`은 (뭐라고 정의했던 지 간에) React를 사용하여 생성된 component에서 접근이 가능하고, React native props에서 접근하여 사용할 수 있다.

```javascript
props.reactProp;
```

[👆](#table-of-contents)

### What is the difference between state and props?

`props`와 `state`는 모두 순수 자바스크립트 오브젝트다. 두 객체 모두 `render`의 output에 영향을 줄 수 있는 정보를 가지고 있지만, 컴포넌트의 기능적인 측면에서는 약간 다르다. `props`는 함수의 파라미터와 비슷한 방식으로 작동하는 반면, `state`는 컴포넌트 내에서 선언된 변수와 비슷하다.

[👆](#table-of-contents)

### Why should we not update the state directly?

`state`를 아래와 같이 바로 업데이트 하면 렌더링이 일어나지 않는다.

```javascript
this.state.message = "Hello world";
```

대신에 `setState()` 메서드를 사용하자.이는 `state`의 변경이 있을 때 `component`를 업데이트 해준다. `state`에 변화가 있을 경우, 컴포넌트는 리렌더링으로 응답한다.

```javascript
//Correct
this.setState({ message: "Hello World" });
```

주의: state를 직접 할당할 수 있는 곳은 `constructor` 혹은 자바스크립트 클래스의 필드를 선언하는 syntax 뿐이다.

[👆](#table-of-contents)

### What is the purpose of callback function as an argument of `setState()`?

콜백함수는 setState가 끝나고 컴포넌트가 렌더링 된 이후에 실행된다.`setState`는 비동기로 이루어지기 때문에 callback에서는 어떤 액션이든 취할 수 있다.

주의: 콜백함수를 사용하는 것보다 라이프사이클 메서드를 사용하는게 더 좋다.

```javascript
setState({ name: "John" }, () =>
  console.log("The name has updated and component re-rendered")
);
```

### What is the difference between HTML and React event handling?

1. HTML에서는 이벤트명은 소문자로 작성되어야 한다.

```html
<button onclick="activateLasers()"></button>
```

React는 camelCase를 사용한다.

```html
<button onClick="{activateLasers}"></button>
```

2. HTML에서는, `false`를 리턴하면 이후 기본 액션을 막을 수 있다.

```html
<a href="#" onclick='console.log("The link was clicked."); return false;' />
```

하지만 react에서는 `preventDefault()`를 명시적으로 사용해야 한다.

```javascript
function handleClick(event) {
  event.preventDefault();
  console.log("The link was clicked.");
}
```

### How to bind methods or event handlers in JSX callbacks?

1. 생성자에서 바인딩하기: 자바스크립트 클래스에서는, 메소드들이 기본적으로 바인딩 되어 있지 않다. 이는 클래스 메서드로 정의된 리액트 이벤트 핸들러와 마찬가지다. 보통, 생성자에서 바인딩한다.

```javascript
class Component extends React.Componenet {
  constructor(props) {
    super(props);
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    // ...
  }
}
```

2. 퍼블리기 클래스 필드 구문: 생성자에서 바인딩 되기를 원치 않는다면, 퍼블릭 클래스의 필드 구문을 이용하여 callback을 올바르게 바인딩 할 수 있다.

```javascript
handleClick = () => {
  console.log("this is:", this);
};

<button onClick={this.handleClick}> Click me </button>;
```

> 클래스 필드(class field)
> 클래스 내부의 캡슐화된 변수를 말한다. 데이터 멤버 또는 멤버 변수라고도 부른다. 클래스 필드는 인스턴스의 프로퍼티 또는 정적 프로퍼티가 될 수 있다. 쉽게 말해, 자바스크립트의 생성자 함수에서 this에 추가한 프로퍼티를 클래스 기반 객체지향 언어에서는 클래스 필드라고 부른다.

```javascript
class Foo {
  name = ""; // SyntaxError

  constructor() {}
}
```

> constructor 내부에서 선언한 클래스 필드는 클래스가 생성할 인스턴스를 가리키는 this에 바인딩한다. 이로써 클래스 필드는 클래스가 생성할 인스턴스의 프로퍼티가 되며, 클래스의 인스턴스를 통해 클래스 외부에서 언제나 참조할 수 있다. 즉, 언제나 public이다.
> ES6의 클래스는 다른 객체지향 언어처럼 private, public, protected 키워드와 같은 접근 제한자(access modifier)를 지원하지 않는다.

3. 화살표함수: 콜백에 화살표 함수를 사용할 수도 있다.

```javascript
<button onClick={event => this.handleClick(event)}>{"Click me"}</button>
```

주의: 콜백이 하위 컴포넌트에 `prop`으로 전달된다면, component가 리렌더링 될 수도 있다. 이러한 경우에는, 성능을 고려해서 1, 2번의 예제를 활용하는 것이 낫다.

[👆](#table-of-contents)

### How to pass a parameter to an event handler or callback?

이벤트 핸들러와 파라미터 전달을ㅇ 화살표 함수로 감쌀 수 있다.

```html
<button onClick={() => this.handleClick(id)} />
```

이는 `.bind`와 같다.

```html
<button onClick="{this.handleClick.bind(this," id)} />
```

두 방식 이외에도, 아래와 같은 배열 함수 방식으로 정의해서 전달할 수도 있다.

```javascript
<button onClick={this.handleClick(id)} />;
handleClick = id => () => {
  console.log("Hello, your ticket number is", id);
};
```

[👆](#table-of-contents)

### What are synthetic events in React?

synthetic event (합성함수) 는 브라우저의 네이티브 이벤트를 위한 크로스 브라우저 래퍼다. 이 api는 브라우저의 네이티브 이벤트와 동일하며, 마찬가지로 `stopPropagation()` `preventDefault()`도 포함하고 있지만, 모든 브라우저에서 동일하게 작동한다는 점이 다르다.

[👆](#table-of-contents)

### What is inline conditional expressions?

조건부 렌더 표현을 위해 javascript의 if문이나 삼항연산자를 사용할 수 있다. 이외에도 중괄호로 묶어서 javascript의 논리식인 &&을 붙여서 jsx에서도 사용할 수 있다.

```html
<h1>Hello!</h1>
; { messages.length > 0 && !isLogin ? (
<h2>You have {messages.length} unread messages.</h2>
) : (
<h2>You don't have unread messages.</h2>
); }
```

[👆](#table-of-contents)

### What are "key" props and what is the benefit of using them in arrays of elements?

`key`는 특별한 string 속성으로, 배열을 사용할 때 이용해야 한다. `key`는 리액트에서 어떤 item이 변화하고, 추가되고, 삭제되었는지 구별하는데 도움을 준다. 대부분 key로 id를 사용한다.

```html
const todoItems = todos.map(todo =>
<li key="{todo.id}">{todo.text}</li>
);
```

만약 이런 ID가 없다면, index를 사용할 수 있다.

```html
const todoItems = todos.map((todo, index) =>
<li key="{index}">
  {todo.text}
</li>
)
```

주의

1. index를 key로 사용하는 방식은, 아이템의 순서가 바뀌는 경우가 발생할 수 있는 케이스에는 별로 추천할만하지 못하다. 이는 퍼포먼스에 악영향을 미치고, component state에 악영향을 미칠 수 있다.
2. list를 별도 컴포넌트로 뽑아서 사용하는 경우, key를 리스트 컴포넌트가 아닌 `li` 태그에 사용해야 한다.
3. 리스트 아이템에 `key`가 없으면 콘솔에 경고 메시지가 뜬다.

### What is the use of refs?

`ref`는 element의 참조값을 반환한다. 대부분 이러한 경우는 피해야 하지만, DOM이나 component에 다이렉트로 접근해야할 때 유용하다.

[👆](#table-of-contents)

### How to create refs?

1. 최근에 추가된 방식으로, `React.createRef()` 메소들를 사용하면, React element는 `ref`를 통해서 접근할 수 있다. `ref`를 컴포넌트에서 접근하기 위해서는, 생성자 안에 `ref`를 instance property로 할당하면 된다.

```javascript
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.myRef = React.createRef();
  }
  render() {
    return <div ref={this.myRef} />;
  }
}
```

2. React 버전과 상관없이 ref 콜백을 활용하는 방식이 있다. 예를 들어, SearchBar 컴포넌트의 인풋 요소들은 아래와 같은 방식으로 접근 가능하다.

```javascript
class SearchBar extends Component {
  constructor(props) {
    super(props);
    this.txtSearch = null;
    this.state = { term: "" };
    this.setInputSearchRef = e => {
      this.txtSearch = e;
    };
  }
  onInputChange(event) {
    this.setState({ term: this.txtSearch.value });
  }
  render() {
    return (
      <input
        value={this.state.term}
        onChange={this.onInputChange.bind(this)}
        ref={this.setInputSearchRef}
      />
    );
  }
}
```

또한 컴포넌트의 함수 내에서 클로져를 `ref`를 사용할 수도 있다.

주의: 추천할만한 방법은 아니지만, 인라인 `ref` callback을 이용하는 방식도 있다.

[👆](#table-of-contents)

### What are forward refs?

Ref forwarding은 일부 컴포넌트에서 ref를 받아서 자식 컴포넌트에게 전달하는 것을 의미한다.

```javascript
const ButtonElement = React.forwardRef((props, ref) => (
  <button ref={ref} className="CustomButton">
    {props.children}
  </button>
));

// Create ref to the DOM button:
const ref = React.createRef();
<ButtonElement ref={ref}>{"Forward Ref"}</ButtonElement>;
```

[👆](#table-of-contents)

### Which is preferred option with in callback refs and findDOMNode()?

callback ref를 쓰는 것이 더 선호된다. 왜냐하면 `findDOMNode()`는 향후에 있을 리액트의 개선사항이 반영되지 않기 때문이다.

레거시에서 `findDOMNode`를 사용하는 방법이 있다.

```javascript
class MyComponent extends Component {
  componentDidMount() {
    findDOMNode(this).scrollIntoView();
  }

  render() {
    return <div />;
  }
}
```

그래서 선호하는 방법은 다음과 같다.

```javascript
class MyComponent extends Component {
  constructor(props) {
    super(props);
    this.node = createRef();
  }
  componentDidMount() {
    this.node.current.scrollIntoView();
  }

  render() {
    return <div ref={this.node} />;
  }
}
```

[👆](#table-of-contents)

### Why are String Refs legacy?

예전에 React를 다뤄보았다면, 옛날 방식인 `ref`를 string으로 쓰는, `ref={'textInput'}` 와 같이 ref속성이 string이고, DOM Node인 `refs.textInput`로 접근하는 방법에 익숙할 것이다. 그러나 이러한 string ref는 하단에서 언급할 문제들 때문에, 레거시로 보는 것이 맞다. 그리고 string ref는 React v16에서 제거 되었다.

1. String ref는 실행중인 component 요소를 추적하도록 강제한다. 그리고 React Module을 stateful하게 만들기 떄문에, 이는 번들시 react module이 중복 되는 경우 이상한 오류를 발생시킨다.
2. 라이브러리를 추가하여 String ref를 child component에 전달한다면, 사용자는 다른 ref를 추가할 수 없다. 그러나 callback ref를 사용하면 이런 문제를 해결할 수 있다.
3. Flow와 같은 정적 분석에서는 동작하지 않는다. Flow는 string ref를 this.refs와 같은 형태로 표시하도록 만드는 트릭을 추적할 수 없다. callback ref는 string ref보다 flow에 더 잘맞다.
4. 대부분이 render callback 패턴으로 동작하기를 기대하지만, 그렇게 동작하지 않는다.

```javascript
class MyComponent extends Component {
  renderRow = index => {
    // 동작하지 않는다. ref는 MyComponent가 아닌 DataTable에 연결될 것이다.
    return <input ref={"input-" + index} />;

    // 이거는 동작한다. callback ref가 짱이다.
    return <input ref={input => (this["input-" + index] = input)} />;
  };

  render() {
    return <DataTable data={this.props.data} renderRow={this.renderRow} />;
  }
}
```

[👆](#table-of-contents)

### What is Virtual DOM?

Virtual DOM은 메모리 내에서 표현되는 Real DOM 이다. UI는 메모리 상에서 표현되며, 그리고 real DOM과 동기화 된다. 이는 렌더 함수 호출과 화면에 elements 표시 하는 사이에 일어난다. 이 모든 과정을 `reconciliation`이라고 한다.

[👆](#table-of-contents)

### How Virtual DOM works?

1. 어디서든 데이터가 편하면, Virtual DOM내에서 전체 UI가 다시 렌덜이 된다.
   ![virtual-dom-1](https://github.com/sudheerj/reactjs-interview-questions/raw/master/images/vdom1.png)

2. 그런 다음 이전 DOM과 새로운 DOM을 비교한다.
   ![virtual-dom-2](https://github.com/sudheerj/reactjs-interview-questions/raw/master/images/vdom2.png)

3. 계산이 끝나면, Real DOM 중에서 실제로 업데이트가 있었던 부분 만 변경을 가한다.
   ![virtual-dom-3](https://github.com/sudheerj/reactjs-interview-questions/raw/master/images/vdom3.png)

[👆](#table-of-contents)

### What is the difference between Shadow DOM and Virtual DOM?

Shadow DOM은 web component의 scope및 CSS scope 지정을 위해 설계된 web browser 기술이다. Virtual DOM은 브라우저 API 위에 자바스크립트에서 구현되는 개념이다.

[👆](#table-of-contents)

### What is React Fiber?

Fiber는 React v16에서 새로운 reconciliation 엔진, 그리고 코어 알고리즘을 새로 작성한 것으로 볼 수 있다. React Fiber의 목적은 애니메이션, 레이아웃, 제스쳐, 작업일시정지 및 중단, 여려 유형의 업데이트 우선순위 조절, 동시성 등 여러가지 기본 사항에 대한 성능을 높이는 것이다.

[👆](#table-of-contents)

### What is the main goal of React Fiber?

React Fiber 의 목표는 애니메이션, 레이아웃, 제스처등의 성능을 높이는 것이다. 렌더링 작업을 chunk별로 작업하고, 여러 프레임 별로 이를 펼치면서 작업하는 점진적 렌더링을 통해 이를 구현했다.

[👆](#table-of-contents)

### What are controlled components?

입력요소를 제어하는 component를 controlled components라고 부른다. 모든 상태변경에 연관뢴 handler function이 존재한다.

예를 들어, 모든 이름을 대문자로 쓰기 위해서는, `handleChange`를 아래와 같이 쓰게 된다.

```javascript
handleChange(event) {
  this.setState({value: event.target.value.toUpperCase()})
}
```

[👆](#table-of-contents)

### What are uncontrolled components?

uncontrolled components란 내부적으로 자기 자신의 state를 가지고 있는 component다. 현재 필요한 값을 찾기 위해 ref를 사용하여 DOM query를 할 수 있다. 이는 전통적인 HTML 과 비슷하다.

`UserProfile` Component를 아래에서 보자면, `name` input이 ref를 통해서 접근할 수 있다.

```javascript
class UserProfile extends React.Component {
  constructor(props) {
    super(props);
    this.handleSubmit = this.handleSubmit.bind(this);
    this.input = React.createRef();
  }

  handleSubmit(event) {
    alert("A name was submitted: " + this.input.current.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          {"Name:"}
          <input type="text" ref={this.input} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

대부분의 경우, 폼에서는 controlled component를 사용하기를 추천한다.

[👆](#table-of-contents)
