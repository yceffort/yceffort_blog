---
title: "리액트 인터뷰 질문 & 답 (2)"
date: 2019-08-21 10:17:16
layout: post
tags: [javascript, react]
---

[목차](/2019/08/13/reactjs-interview-questions/)

## Table of Contents

| No. | Questions                                                                                                                                                                        |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | **React Router**                                                                                                                                                                 |
| 129 | [What is React Router?](#what-is-react-router)                                                                                                                                   |
| 130 | [How React Router is different from history library?](#how-react-router-is-different-from-history-library)                                                                       |
| 131 | [What are the \<Router> components of React Router v4?](#what-are-the-router-components-of-react-router-v4)                                                                      |
| 132 | [What is the purpose of push and replace methods of history?](#what-is-the-purpose-of-push-and-replace-methods-of-history)                                                       |
| 133 | [How do you programmatically navigate using React router v4?](#how-do-you-programmatically-navigate-using-react-router-v4)                                                       |
| 134 | [How to get query parameters in React Router v4](#how-to-get-query-parameters-in-react-router-v4)                                                                                |
| 135 | [Why you get "Router may have only one child element" warning?](#why-you-get-router-may-have-only-one-child-element-warning)                                                     |
| 136 | [How to pass params to history.push method in React Router v4?](#how-to-pass-params-to-historypush-method-in-react-router-v4)                                                    |
| 137 | [How to implement default or NotFound page?](#how-to-implement-default-or-notfound-page)                                                                                         |
| 138 | [How to get history on React Router v4?](#how-to-get-history-on-react-router-v4)                                                                                                 |
| 139 | [How to perform automatic redirect after login?](#how-to-perform-automatic-redirect-after-login)                                                                                 |
|     | **React Internationalization**                                                                                                                                                   |
| 140 | [What is React-Intl?](#what-is-react-intl)                                                                                                                                       |
| 141 | [What are the main features of React Intl?](#what-are-the-main-features-of-react-intl)                                                                                           |
| 142 | [What are the two ways of formatting in React Intl?](#what-are-the-two-ways-of-formatting-in-react-intl)                                                                         |
| 143 | [How to use FormattedMessage as placeholder using React Intl?](#how-to-use-formattedmessage-as-placeholder-using-react-intl)                                                     |
| 144 | [How to access current locale with React Intl](#how-to-access-current-locale-with-react-intl)                                                                                    |
| 145 | [How to format date using React Intl?](#how-to-format-date-using-react-intl)                                                                                                     |
|     | **React Testing**                                                                                                                                                                |
| 146 | [What is Shallow Renderer in React testing?](#what-is-shallow-renderer-in-react-testing)                                                                                         |
| 147 | [What is TestRenderer package in React?](#what-is-testrenderer-package-in-react)                                                                                                 |
| 148 | [What is the purpose of ReactTestUtils package?](#what-is-the-purpose-of-reacttestutils-package)                                                                                 |
| 149 | [What is Jest?](#what-is-jest)                                                                                                                                                   |
| 150 | [What are the advantages of Jest over Jasmine?](#what-are-the-advantages-of-jest-over-jasmine)                                                                                   |
| 151 | [Give a simple example of Jest test case](#give-a-simple-example-of-jest-test-case)                                                                                              |
|     | **React Redux**                                                                                                                                                                  |
| 152 | [What is Flux?](#what-is-flux)                                                                                                                                                   |
| 153 | [What is Redux?](#what-is-redux)                                                                                                                                                 |
| 154 | [What are the core principles of Redux?](#what-are-the-core-principles-of-redux)                                                                                                 |
| 155 | [What are the downsides of Redux compared to Flux?](#what-are-the-downsides-of-redux-compared-to-flux)                                                                           |
| 156 | [What is the difference between mapStateToProps() and mapDispatchToProps()?](#what-is-the-difference-between-mapstatetoprops-and-mapdispatchtoprops)                             |
| 157 | [Can I dispatch an action in reducer?](#can-i-dispatch-an-action-in-reducer)                                                                                                     |
| 158 | [How to access Redux store outside a component?](#how-to-access-redux-store-outside-a-component)                                                                                 |
| 159 | [What are the drawbacks of MVW pattern](#what-are-the-drawbacks-of-mvw-pattern)                                                                                                  |
| 160 | [Are there any similarities between Redux and RxJS?](#are-there-any-similarities-between-redux-and-rxjs)                                                                         |
| 161 | [How to dispatch an action on load?](#how-to-dispatch-an-action-on-load)                                                                                                         |
| 162 | [How to use connect from React Redux?](#how-to-use-connect-from-react-redux)                                                                                                     |
| 163 | [How to reset state in Redux?](#how-to-reset-state-in-redux)                                                                                                                     |
| 164 | [Whats the purpose of at symbol in the redux connect decorator?](#whats-the-purpose-of-at-symbol-in-the-redux-connect-decorator)                                                 |
| 165 | [What is the difference between React context and React Redux?](#what-is-the-difference-between-react-context-and-react-redux)                                                   |
| 166 | [Why are Redux state functions called reducers?](#why-are-redux-state-functions-called-reducers)                                                                                 |
| 167 | [How to make AJAX request in Redux?](#how-to-make-ajax-request-in-redux)                                                                                                         |
| 168 | [Should I keep all component's state in Redux store?](#should-i-keep-all-components-state-in-redux-store)                                                                        |
| 169 | [What is the proper way to access Redux store?](#what-is-the-proper-way-to-access-redux-store)                                                                                   |
| 170 | [What is the difference between component and container in React Redux?](#what-is-the-difference-between-component-and-container-in-react-redux)                                 |
| 171 | [What is the purpose of the constants in Redux? ](#what-is-the-purpose-of-the-constants-in-redux)                                                                                |
| 172 | [What are the different ways to write mapDispatchToProps()?](#what-are-the-different-ways-to-write-mapdispatchtoprops)                                                           |
| 173 | [What is the use of the ownProps parameter in mapStateToProps() and mapDispatchToProps()?](#what-is-the-use-of-the-ownprops-parameter-in-mapstatetoprops-and-mapdispatchtoprops) |
| 174 | [How to structure Redux top level directories?](#how-to-structure-redux-top-level-directories)                                                                                   |
| 175 | [What is redux-saga?](#what-is-redux-saga)                                                                                                                                       |
| 176 | [What is the mental model of redux-saga?](#what-is-the-mental-model-of-redux-saga)                                                                                               |
| 177 | [What are the differences between call and put in redux-saga](#what-are-the-differences-between-call-and-put-in-redux-saga)                                                      |
| 178 | [What is Redux Thunk?](#what-is-redux-thunk)                                                                                                                                     |
| 179 | [What are the differences between redux-saga and redux-thunk](#what-are-the-differences-between-redux-saga-and-redux-thunk)                                                      |
| 180 | [What is Redux DevTools?](#what-is-redux-devtools)                                                                                                                               |
| 181 | [What are the features of Redux DevTools?](#what-are-the-features-of-redux-devtools)                                                                                             |
| 182 | [What are Redux selectors and Why to use them?](#what-are-redux-selectors-and-why-to-use-them)                                                                                   |
| 183 | [What is Redux Form?](#what-is-redux-form)                                                                                                                                       |
| 184 | [What are the main features of Redux Form?](#what-are-the-main-features-of-redux-form)                                                                                           |
| 185 | [How to add multiple middlewares to Redux?](#how-to-add-multiple-middlewares-to-redux)                                                                                           |
| 186 | [How to set initial state in Redux?](#how-to-set-initial-state-in-redux)                                                                                                         |
| 187 | [How Relay is different from Redux?](#how-relay-is-different-from-redux)                                                                                                         |
|     | **React Native**                                                                                                                                                                 |
| 188 | [What is the difference between React Native and React?](#what-is-the-difference-between-react-native-and-react)                                                                 |
| 189 | [How to test React Native apps?](#how-to-test-react-native-apps)                                                                                                                 |
| 190 | [How to do logging in React Native?](#how-to-do-logging-in-react-native)                                                                                                         |
| 191 | [How to debug your React Native?](#how-to-debug-your-react-native)                                                                                                               |
|     | **React supported libraries and Integration**                                                                                                                                    |
| 192 | [What is reselect and how it works?](#what-is-reselect-and-how-it-works)                                                                                                         |
| 193 | [What is Flow?](#what-is-flow)                                                                                                                                                   |
| 194 | [What is the difference between Flow and PropTypes?](#what-is-the-difference-between-flow-and-proptypes)                                                                         |
| 195 | [How to use font-awesome icons in React?](#how-to-use-font-awesome-icons-in-react)                                                                                               |
| 196 | [What is React Dev Tools?](#what-is-react-dev-tools)                                                                                                                             |
| 197 | [Why is DevTools not loading in Chrome for local files?](#why-is-devtools-not-loading-in-chrome-for-local-files)                                                                 |
| 198 | [How to use Polymer in React?](#how-to-use-polymer-in-react)                                                                                                                     |
| 199 | [What are the advantages of React over Vue.js?](#what-are-the-advantages-of-react-over-vuejs)                                                                                    |
| 200 | [What is the difference between React and Angular?](#what-is-the-difference-between-react-and-angular)                                                                           |
| 201 | [Why React tab is not showing up in DevTools?](#why-react-tab-is-not-showing-up-in-devtools)                                                                                     |
| 202 | [What are styled components?](#what-are-styled-components)                                                                                                                       |
| 203 | [Give an example of Styled Components?](#give-an-example-of-styled-components)                                                                                                   |
| 204 | [What is Relay?](#what-is-relay)                                                                                                                                                 |
| 205 | [How to use TypeScript in create-react-app application?](#how-to-use-typescript-in-create-react-app-application)                                                                 |

## React Router

### What is React Router?

React Router는 리액트 최상단에 있는 강력한 라우팅 라이브러리로, 페이지에 보여주는 내용과 URL사이에 동기화를 유지해주고, 어플리케이션에 새로운 화면과 흐름을 추가할 수 있도록 도와준다.

[👆](#table-of-contents)

### How React Router is different from history library?

React router는 history라이브러리를 감싼 래퍼로, 브라우저의 `window.history`와 상호작용하고, 브라우저 및 해쉬의 히스토리를 다룬다. 또한 모바일 앱 개발 (React Native) 및 Node의 unit testing처럼 global histroy가 없는 환경에 유용한 메모리 히스토리를 제공한다.

[👆](#table-of-contents)

### What are the `<Router>` components of React Router v4?

v4는 새로운 3개의 `<Router>` 컴포넌트를 제공한다.

1. `<BrowserRouter>`
2. `<HashRouter>`
3. `<MemoryRouter>`

위 컴포넌트는 각각 브라우저, 해쉬, 메모리 히스토리 인스턴스를 만들어준다. React Router v4는 Router Object의 context를 통해, history 인스턴스의 속성과 메소드를 활용할 수 있게 해준다.

[👆](#table-of-contents)

### What is the purpose of `push()` and `replace()` methods of `history`?

히스토리 인스턴스에는 네비게이션 목적으로 두개의 메소드를 제공한다.

1. `push()`
2. `replace()`

만약 히스토리가 방문했던 곳들의 배열이라고 생각한다면, `push()`가 그 역할을 할 것이고, 현재 위치를 덮어쓰는 느낌을 원한다면 `replace()`가 맞을 것이다.

[👆](#table-of-contents)

### How do you programmatically navigate using React Router v4?

Component 내에서 프로그래밍으로 라우팅/네비게이팅 하는 방법에는 3가지가 있다.

1. HOF에서 `withRouter()`를 쓰는법
   HOF의 `withRouter()`는 컴포넌트의 prop에 히스토리 오브젝트를 인젝트 한다. 이 오브젝트는 `push()` `replace()`를 제공하여 context의 사용을 피하게 해준다.

```javascript
import { withRouter } from "react-router-dom"; // this also works with 'react-router-native'

const Button = withRouter(({ history }) => (
  <button
    type="button"
    onClick={() => {
      history.push("/new-location");
    }}
  >
    {"Click Me!"}
  </button>
));
```

2. `<Route>` 컴포넌트와 render props 패턴을 사용하는 법
   `<Route>`는 `withRouter()`와 같은 props를 넘기므로, history prop을 통해 histoy 메서드에 접근할 수 있을 것이다.

```javascript
import { Route } from "react-router-dom";

const Button = () => (
  <Route
    render={({ history }) => (
      <button
        type="button"
        onClick={() => {
          history.push("/new-location");
        }}
      >
        {"Click Me!"}
      </button>
    )}
  />
);
```

3. Context
   이 방식은 딱히 추천되지 않고, 불안정한 API 활용으로 간주된다.

```javascript
const Button = (props, context) => (
  <button
    type="button"
    onClick={() => {
      context.history.push("/new-location");
    }}
  >
    {"Click Me!"}
  </button>
);

Button.contextTypes = {
  history: React.PropTypes.shape({
    push: React.PropTypes.func.isRequired
  })
};
```

[👆](#table-of-contents)

### How to get query parameters in React Router v4?

수년간 다른 구현 지원에 대한 사용자들의 많은 요청 떄문에, React Router v4에서는 query string을 parsing 하는 방법은 사라졌다. 이는 유저가 원하는 대로 구현할 수 있는 자유도를 주었다. 추천하는 방법은, query string 라이브러리를 사용하는 것이다.

```javascript
const queryString = require("query-string");
const parsed = queryString.parse(props.location.search);
```

native 방식을 선호한다면 `URLSearchParam`을 사용할 수도 있다.

```javascript
const params = new URLSearchParams(props.location.search);
const foo = params.get("name");
```

다만 IE11에서는 폴리필이 필요하다.

[👆](#table-of-contents)

### Why you get "Router may have only one child element" warning?

Route는 `<Switch>` 블록으로 감싸줘야 하는데, 왜냐하면 `<Switch>`는 라우트를 베타적으로 감싸기 때문이다. 먼저 `Switch`를 임포트 해야 한다.

```javascript
import { Switch, Router, Route } from "react-router";
```

그리고 route를 `<Switch>` 블록에 넣어햐 한다.

```html
<Router>
  <Switch>
    <Route {/* ... */} /> <Route {/* ... */} />
  </Switch>
</Router>
```

[👆](#table-of-contents)

### How to pass params to `history.push` method in React Router v4?

history 객체에 props를 보낼 수 있다.

```javascript
this.props.history.push({
  pathname: "/template",
  search: "?name=sudheer",
  state: { detail: response.data }
});
```

`search` 속성은 `push()`에서 query param을 보낼 때 사용된다.

[👆](#table-of-contents)

### How to implement _default_ or _NotFound_ page?

`<Switch>`는 첫번째로 일치하는 `<Route>`를 렌더링한다. path가 없는 route는 항상 매치하게 되어 있다. 따라서, path를 제거한 route를 하나 추가하면 된다.

```javascript
<Switch>
  <Route exact path="/" component={Home} />
  <Route path="/user" component={User} />
  <Route component={NotFound} />
</Switch>
```

[👆](#table-of-contents)

### How to get history on React Router v4?

1. history 오브젝트를 익스포트 하는 모듈을 만들고, 프로젝트 전체에서 해당 모듈을 임포트 한다. 예를들어,

```javascript
import { createBrowserHistory } from "history";

export default createBrowserHistory({
  /* pass a configuration object here if needed */
});
```

2. 빌트인 라우터 대신에, `<Router>` 컴포넌트를 쓴다. 위에서 만든 `history.js`를 `index.js`에 임포트 한다.

```javascript
import { Router } from "react-router-dom";
import history from "./history";
import App from "./App";

ReactDOM.render(
  <Router history={history}>
    <App />
  </Router>,
  holder
);
```

3. 빌트인 히스토리 오브젝트와 비슷하게, history의 push메소드를 쓸수도 있다.

```javascript
// some-other-file.js
import history from "./history";

history.push("/go-here");
```

[👆](#table-of-contents)

### How to perform automatic redirect after login?

`react-router`sms `<Redirect>` 컴포넌트를 제공한다. `<Redirect>`를 렌더링 하면 새로운 위치로 이동하게 된다. 서버사이드 리다이렉트와 마찬가지로, 새로운 위치는 현재 히스토리 스택에 있는 현재 위치를 덮어쓰게 된다.

```javascript
import React, { Component } from "react";
import { Redirect } from "react-router";

export default class LoginComponent extends Component {
  render() {
    if (this.state.isLoggedIn === true) {
      return <Redirect to="/your/redirect/page" />;
    } else {
      return <div>{"Login Please"}</div>;
    }
  }
}
```

[👆](#table-of-contents)

## React Internationalization

### What is React Intl?

[👆](#table-of-contents)

### What are the main features of React Intl?

[👆](#table-of-contents)

### What are the two ways of formatting in React Intl?

[👆](#table-of-contents)

### How to use `<FormattedMessage>` as placeholder using React Intl?

[👆](#table-of-contents)

### How to access current locale with React Intl?

[👆](#table-of-contents)

### How to format date using React Intl?

[👆](#table-of-contents)

## React Testing

### What is Shallow Renderer in React testing?

[👆](#table-of-contents)

### What is `TestRenderer` package in React?

[👆](#table-of-contents)

### What is the purpose of ReactTestUtils package?

[👆](#table-of-contents)

### What is Jest?

[👆](#table-of-contents)

### What are the advantages of Jest over Jasmine?

[👆](#table-of-contents)

### Give a simple example of Jest test case

[👆](#table-of-contents)

## React Redux

### What is flux?

[👆](#table-of-contents)

### What is Redux?

[👆](#table-of-contents)

### What are the core principles of Redux?

[👆](#table-of-contents)

### What are the downsides of Redux compared to Flux?

[👆](#table-of-contents)

### What is the difference between `mapStateToProps()` and `mapDispatchToProps()`?

[👆](#table-of-contents)

### Can I dispatch an action in reducer?

[👆](#table-of-contents)

### How to access Redux store outside a component?

[👆](#table-of-contents)

### What are the drawbacks of MVW pattern?

[👆](#table-of-contents)

### Are there any similarities between Redux and RxJS?

[👆](#table-of-contents)

### How to dispatch an action on load?

[👆](#table-of-contents)

### How to use `connect()` from React Redux?

[👆](#table-of-contents)

### How to reset state in Redux?

[👆](#table-of-contents)

### Whats the purpose of `at` symbol in the Redux connect decorator?

[👆](#table-of-contents)

### What is the difference between React context and React Redux?

[👆](#table-of-contents)

### Why are Redux state functions called reducers?

[👆](#table-of-contents)

### How to make AJAX request in Redux?

[👆](#table-of-contents)

### Should I keep all component's state in Redux store?

[👆](#table-of-contents)

### What is the proper way to access Redux store?

[👆](#table-of-contents)

### What is the difference between component and container in React Redux?

[👆](#table-of-contents)

### What is the purpose of the constants in Redux?

[👆](#table-of-contents)

### What are the different ways to write `mapDispatchToProps()`?

[👆](#table-of-contents)

### What is the use of the `ownProps` parameter in `mapStateToProps()` and `mapDispatchToProps()`?

[👆](#table-of-contents)

### How to structure Redux top level directories?

[👆](#table-of-contents)

### What is redux-saga?

[👆](#table-of-contents)

### What is the mental model of redux-saga?

[👆](#table-of-contents)

### What are the differences between `call()` and `put()` in redux-saga?

[👆](#table-of-contents)

### What is Redux Thunk?

[👆](#table-of-contents)

### What are the differences between `redux-saga` and `redux-thunk`?

[👆](#table-of-contents)

### What is Redux DevTools?

[👆](#table-of-contents)

### What are the features of Redux DevTools?

[👆](#table-of-contents)

### What are Redux selectors and why to use them?

[👆](#table-of-contents)

### What is Redux Form?

[👆](#table-of-contents)

### What are the main features of Redux Form?

[👆](#table-of-contents)

### How to add multiple middlewares to Redux?

[👆](#table-of-contents)

### How to set initial state in Redux?

[👆](#table-of-contents)

### How Relay is different from Redux?

## React Native

### What is the difference between React Native and React?

[👆](#table-of-contents)

### How to test React Native apps?

[👆](#table-of-contents)

### How to do logging in React Native?

[👆](#table-of-contents)

### How to debug your React Native?

[👆](#table-of-contents)

## React supported libraries & Integration

### What is reselect and how it works?

[👆](#table-of-contents)

### What is Flow?

[👆](#table-of-contents)

### What is the difference between Flow and PropTypes?

[👆](#table-of-contents)

### How to use Font Awesome icons in React?

[👆](#table-of-contents)

### What is React Dev Tools?

[👆](#table-of-contents)

### Why is DevTools not loading in Chrome for local files?

[👆](#table-of-contents)

### How to use Polymer in React?

[👆](#table-of-contents)

### What are the advantages of React over Vue.js?

[👆](#table-of-contents)

### What is the difference between React and Angular?

[👆](#table-of-contents)

### Why React tab is not showing up in DevTools?

[👆](#table-of-contents)

### What are Styled Components?

[👆](#table-of-contents)

### Give an example of Styled Components?

[👆](#table-of-contents)

### What is Relay?

[👆](#table-of-contents)

### How to use TypeScript in `create-react-app` application?

[👆](#table-of-contents)
