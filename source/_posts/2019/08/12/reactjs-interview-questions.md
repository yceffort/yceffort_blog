---
title: "리액트 인터뷰 질문 & 답"
date: 2019-08-13 16:22:35
layout: post
tags: [browser]
---

### 🚧작성중 🚧

[원문-reactjs-interview-questions](https://github.com/sudheerj/reactjs-interview-questions)


### Table of Contents

| No. | Questions                                                                               |
| --- | --------------------------------------------------------------------------------------- |
|     | **Core React**                                                                          |
| 1   | [리액트란 무엇인가?](#what-is-react)                                                            |
| 2   | [리액트의 주요 기능은 무엇인가?](#what-are-the-major-features-of-react)                              |
| 3   | [JSX란 무엇인가?](#what-is-jsx)                                                              |
| 4   | [element와 component의 차이점은 무엇인가?](#what-is-the-difference-between-element-and-component) |
| 5   | [리액트에서 컴포넌트를 어떻게 만드는가?](#how-to-create-components-in-react)                             |


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
    return(
      <div>
        <h1>{'Welcome to React world!'}</h1>
      </div>
    )
  }
}
```

[👆](#table-of-contents)

### What is the difference between Element and Component?

`element`는 DOM노드나 컴포넌트 단에서 화면에 보여주고 싶은 요소를 그리는 하나의 오브젝트를 의미한다. `element`는 `element`의 props에서 포함될 수 있다. 리액트에서 `element`를 만드는건 많은 비용이 들지 않는다. 한번 만들고 나면, 더이상 변경이 불가능하다. 

리액트에서 `element`를 만드는 예시는 아래와 같다.

```javascript
const element = React.createElement(
  'div',
  {id: 'login-btn'},
  'Login'
)
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
<div id='login-btn'>Login</div>
```

반면에 컴포넌트는 다양한 방식으로 선언가능하다. 컴포넌트는 `render()`와 함께 쓴다면 클래스가 될 수도 있다. 좀더 단순한 방법으로, 함수로도 선언이 될 수 있다. 두 방식 모두 `props`를 input으로 받으며, `JSX`를 리턴한다.

```javascript
const Button = ({ onLogin }) =>
  <div id={'login-btn'} onClick={onLogin}>Login</div>
```

JSX는 이를 `React.createElement()` 함수로 트랜스파일 시킬 것이다.

```html
const Button = ({ onLogin }) => React.createElement(
  'div',
  { id: 'login-btn', onClick: onLogin },
  'Login'
)
```

[👆](#table-of-contents)

### How to create components in React?

두 가지 방법이 존재한다.

   1. 함수형 컴포넌트: 컴포넌트를 만드는 가장 심플한 방식이다. `props`를 첫번째 파라미터로 받는 받는 순수 자바스크립트 함수를 만들고, React Element를 반환하면 된다.
   ```javascript
   function Greeting({ message }) {
        return <h1>{`Hello, ${message}`}</h1>
    }
   ```
   1. 클래스 컴포넌트: ES6의 클래스를 활용하여 컴포넌트를 정의할 수도 있다. 위 컴포넌트를 클래스 컴포넌트로 바꾼다면 이렇게 될 것이다.
   ```javascript
    class Greeting extends React.Component {
    render() {
        return <h1>{`Hello, ${this.props.message}`}</h1>
        }
    }
   ```

[👆](#table-of-contents)