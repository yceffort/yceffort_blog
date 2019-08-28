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

수년간 다른 구현 지원에 대한 사용자들의 많은 요청 때문에, React Router v4에서는 query string을 parsing 하는 방법은 사라졌다. 이는 유저가 원하는 대로 구현할 수 있는 자유도를 주었다. 추천하는 방법은, query string 라이브러리를 사용하는 것이다.

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

React Intl string, dates, numbers, 복수 표현 등을 다국어로 포맷팅할 수 있는 컴포넌트와 API를 제공한다. React Intl는 components 와 API 를 바탕으로 Reac를 바인딩하는 FormatJS 의 일부분이다.

[👆](#table-of-contents)

### What are the main features of React Intl?

1. 숫자를 , 와 함께 표현
2. 날짜와 시간을 올바르게 표현
3. 현재시간을 기준으로 날자를 표현
4. string의 복수표현
5. 150+개의 언어 지원
6. 브라우저와 노드에서 실행
7. 표준에 맞춰 제작

[👆](#table-of-contents)

### What are the two ways of formatting in React Intl?

string, number, date를 포맷팅하는 방법은 react 컴포넌트 또는 api를 사용하는 두가지 방법이 있다.

```jsx harmony
<FormattedMessage
  id={"account"}
  defaultMessage={"The amount is less than minimum balance."}
/>
```

```javascript
const messages = defineMessages({
  accountMessage: {
    id: "account",
    defaultMessage: "The amount is less than minimum balance."
  }
});

formatMessage(messages.accountMessage);
```

[👆](#table-of-contents)

### How to use `<FormattedMessage>` as placeholder using React Intl?

`<Formatted... />` 컴포넌트는 plain text가 아닌 elements를 반환하므로, placeholder, alt text처럼 string이 필요한 곳에는 쓸 수 없다. 따라서 여기에서는 `formatMessage()`를 사용해야한다. higher-order component인 injectIntl()을 사용하여, 컴포넌트에 intl 객체를 주입하고, 객체에서 사용할 수 있는 `formatMessage()`를 사용하여 message를 포맷팅할 수 있다.

```jsx harmony
import React from "react";
import { injectIntl, intlShape } from "react-intl";

const MyComponent = ({ intl }) => {
  const placeholder = intl.formatMessage({ id: "messageId" });
  return <input placeholder={placeholder} />;
};

MyComponent.propTypes = {
  intl: intlShape.isRequired
};

export default injectIntl(MyComponent);
```

[👆](#table-of-contents)

### How to access current locale with React Intl?

어느 어플리케이션에서든 `injectIntl()`를 사용하면 현재 로케일을 얻을 수 있다.

[👆](#table-of-contents)

### How to format date using React Intl?

higher-order 컴포넌트 `injectIntl()`는 컴포넌트의 props에 `formatDate()`메서드를 제공한다. 이 메서드는 내부적으로 `FormattedDate`인스턴스를 활용하고, 이는 포맷된 날짜를 string으로 제공한다.

```jsx harmony
import { injectIntl, intlShape } from "react-intl";

const stringDate = this.props.intl.formatDate(date, {
  year: "numeric",
  month: "numeric",
  day: "numeric"
});

const MyComponent = ({ intl }) => (
  <div>{`The formatted date is ${stringDate}`}</div>
);

MyComponent.propTypes = {
  intl: intlShape.isRequired
};

export default injectIntl(MyComponent);
```

[👆](#table-of-contents)

## React Testing

### What is Shallow Renderer in React testing?

`Shallow rendering`는 React에서 유닛테스트 케이스를 작성할 때 유용하다. 이는 컴포넌트를 한단계 더 깊이 렌더링하며, 렌더링되지 않은 하위 컴포넌트에 대한 고민 ㅇ벗이 렌더링 메서드가 반환하는 것에 대해 asset를 수행할 수 있다.

```jsx harmony
function MyComponent() {
  return (
    <div>
      <span className={"heading"}>{"Title"}</span>
      <span className={"description"}>{"Description"}</span>
    </div>
  );
}
```

```javascript
import ShallowRenderer from "react-test-renderer/shallow";

const renderer = new ShallowRenderer();
renderer.render(<MyComponent />);

const result = renderer.getRenderOutput();

expect(result.type).toBe("div");
expect(result.props.children).toEqual([
  <span className={"heading"}>{"Title"}</span>,
  <span className={"description"}>{"Description"}</span>
]);
```

[👆](#table-of-contents)

### What is `TestRenderer` package in React?

`TestRenderer` 패키지는 component 를 DOM 또는 Native mobile 환경에 의존없이 순수 Javascript Object 로 렌더링 할 수 있는 renderer 를 제공한다. 이 패키지를 사용하면 브라우저 또는 jsdom 의 사용없이 ReactDOM 또는 React Native 에서 렌더링 되는 플랫폼의 뷰 계층구조 (DOM 트리와 유사) 의 스냅샷을 쉽게 가져올 수 있다.

```jsx harmony
import TestRenderer from "react-test-renderer";

const Link = ({ page, children }) => <a href={page}>{children}</a>;

const testRenderer = TestRenderer.create(
  <Link page={"https://www.facebook.com/"}>{"Facebook"}</Link>
);

console.log(testRenderer.toJSON());
// {
//   type: 'a',
//   props: { href: 'https://www.facebook.com/' },
//   children: [ 'Facebook' ]
// }
```

[👆](#table-of-contents)

### What is the purpose of ReactTestUtils package?

`ReactTestUtils`는 유닛테스트를 목적으로 DOM을 조작할 수 있는 `with-addons`패키지를 제공한다.

[👆](#table-of-contents)

### What is Jest?

Jest는 페이스북이 만든 자바스크립트 유닛테스트 프레임워크로, Jasmine을 기반으로 만들어 졌으며 자동 mock 생성, `jsdom` 환경 제공 등의 기능을 제공한다. 컴포넌트를 테스트 하는데 사용 된다.

[👆](#table-of-contents)

### What are the advantages of Jest over Jasmine?

Jasmine보다 Jest가 더 좋은 점은

- 소스코드에서 자동으로 테스트 코드를 찾아서 테스트
- 테스트 시 자동으로 mock 의 존성 참고
- 동기로 작성된 코드를 비동기로 테스트
- fake Dom implementation으로 테스트 하여, 명령줄에서도 테스트 가능
- 병렬 프로세스로 테스트 하여 테스트가 더욱 빠르게 수행됨

[👆](#table-of-contents)

### Give a simple example of Jest test case

두 숫자를 더하는 `sum.js`를 작성한다.

```javascript
const sum = (a, b) => a + b;
export default sum;
```

테스트를 수행하는 `sum.test.js`를 작성

```javascript
import sum from "./sum";

test("adds 1 + 2 to equal 3", () => {
  expect(sum(1, 2)).toBe(3);
});
```

`package.json`에 테스트를 실행하는 코드 추가

```json
{
  "scripts": {
    "test": "jest"
  }
}
```

`yarn test` `npm test`로 테스트 실행 및 결과 확인

```shell
$ yarn test
PASS ./sum.test.js
✓ adds 1 + 2 to equal 3 (2ms)
```

[👆](#table-of-contents)

## React Redux

### What is flux?

Flux는 어플리케이션 디자인 패러다임으로, 전통적인 모델인 MVC pattern을 대체하기 위해 나왔다. Flux는 프레임워크나 라이브러리가 아닌, React와 양방향 데이터 흐름을 기반으로 하는 새로운 아키텍쳐다. 페이스북이 React를 사용할 때 내부적으로 이 패턴을 활용한다.

dispatcher, sotres, views 컴포넌트 사이 작업흐름은 아래처럼 input과 output이 구별되어 나타난다.

![flux-diagram](https://github.com/sudheerj/reactjs-interview-questions/raw/master/images/flux.png)

[👆](#table-of-contents)

### What is Redux?

Redux는 flux 디자인 패턴을 기반으로 한 자바스크립트 앱의 예측가능한 state container다. Redux는 React또는 다른 어떤 뷰 라이브러리와 함께 사용할 수 있다. Redux는 크기가 매우 작고 (2kb), 다른 디펜던시를 갖고 있지 않다.

[👆](#table-of-contents)

### What are the core principles of Redux?

Redux는 다음 세가지 기본 원칙을 가지고 있다.

1. 신뢰할 수 있는 단일 출처: 어플리케이션의 state는 단일 store에 객체트리 형태로 저장되어 있다. 단일 state tree는 변화를 쉽게 추적ㄷ할 수 있게 해주며, 어플리케이션을 디버그하고 검사하는 것을 쉽게 만들어 준다.
2. state는 읽기 전용: state를 변경할 수 있는 방법은 단한가지로, 객체가 어떤 일이 일어났는지 묘사하는 액션을 보내는 것이다. 이는 views나 네트워크 콜백이 직접 state를 수정하지 않도록 한다.
3. 변화는 순수 함수로만 이루어진다: 액션별로 state 트리가 어떻게 변화하는지 명세하기 위해, reducer를 사용해야 한다.

[👆](#table-of-contents)

### What are the downsides of Redux compared to Flux?

Flux와 비교했을 때, Redux는 몇가지 단점을 가지고 있다.

1. 변이를 피하는 법을 배워야 한다: Flux는 데이터 변이에 대해 특별한 의견이 없지만, Redux는 데이터 변이를 선호하지 않으며, 다른 추가 보완 패키지를 활용하여 이를 유지한다. dev-only 패지지인 `redux-immutable-state-invariant`나 `Immutable.js`를 활용하거나, 팀원들에게 변이 없는 코드에 대해 방법론을 확산해야 한다.
2. 패키지를 고를때 신중해진다: Flux는 undo/redo, 지속성, 폼 관련 문제에 대해 무관심하지만, Redux 는 미들웨어 및 Store 개선 등 확장된 포인트들을 가지고 풍부한 생태계를 만들어 냈기 때문에, 패키지 선택에 주의가 필요하다.
3. 타입체크: Flux는 정적 타입 체크를 할 수 있는 방법이 있지만, Redux는 아직 지원하고 있지 않다.

[👆](#table-of-contents)

### What is the difference between `mapStateToProps()` and `mapDispatchToProps()`?

`mapStateToProps()`는 컴포넌트에서 다른 컴포넌트에 의해 업데이트된 state를 가져올수 있도록 도와주는 유틸리티다.

```javascript
const mapStateToProps = state => {
  return {
    todos: getVisibleTodos(state.todos, state.visibilityFilter)
  };
};
```

`mapDispatchToProps()`는 컴포넌트가 이벤트를 발생시킬 수 있도록 도와주는 유틸리티다. (이 이벤트는 어플리케이션의 state에 변화를 가져올 수 있음)

```javascript
const mapDispatchToProps = dispatch => {
  return {
    onTodoClick: id => {
      dispatch(toggleTodo(id));
    }
  };
};
```

`mapDispatchToProps`에서는 항상 객체를 파라미터로 보내기를 권장한다.

Redux는 `(…args) => dispatch(onTodoClick(…args))`와 같은 형태의 다른 함수로 감싸고, 이렇게 감싼 함수를 컴포넌트의 prop로 전달한다.

```javascript
const mapDispatchToProps = {
  onTodoClick
};
```

[👆](#table-of-contents)

### Can I dispatch an action in reducer?

Reducer안에서 액션을 보내는 것은 안티패턴이다. Reducer는 사이드이펙트를 최소화 하기 위하여, 단순히 액션에 대한 처리와 새로운 state를 가진 object를 반환하기만 해야 한다. Reducer내에서 리스너를 달고, 액션을 보내는 것은 다른 액션과 연쇄작용을 일으킬 수도 있으며, 사이드 이펙트를 야기할 수도 있다.

[👆](#table-of-contents)

### How to access Redux store outside a component?

`createStore()`로 만들어진 모듈을 export 하면 된다. 그리고 global 객체인 window를 사용해서는 안된다.

```javascript
store = createStore(myReducer);

export default store;
```

[👆](#table-of-contents)

### What are the drawbacks of MVW pattern?

1. DOM 조작은, 많은 비용을 지불해야 하고, 어플리케이션을 느리고 비효율적으로 만든다.
2. 순환 참조로 인해, 복잡한 모델이 모델과 뷰주변에 만들어질 수 있다.
3. 구글 docs와 같은 협업 어플리케이션에서는 많은 양의 데이터 변경이 일어날 수 있다.
4. 추가적으로 많은 코드를 쓰지 않고 undo를 쉽게 할 수 없다.

[👆](#table-of-contents)

### Are there any similarities between Redux and RxJS?

두 라이브러리는 목적부터 완전히 다르지만, 약간의 비슷한점을 가지고있다.

Redux는 어플리케이션 전반에서 state를 관리할 수 있게 도와주는 툴이다. 이는 보통 UI 아키텍쳐에서 ㅁ낳이 사용된다. Angular의 대체재라고 볼 수 있다. 반면 Rxjs는 반응형 프로그래밍 라이브러리다. RxJS는 자바스크립트에서 비동기 작업을 수행하기 위해 사용된다. Promise의 대체재라고 볼 수있다. Redux는 Store가 반응형이기 때문에 반응형 패러다임을 사용한다. Store는 액션을 어느정도 거리에서 관찰하다가, 스스로 변화한다. RxJS 또한 반응형 패러다임을 사용하는 반면, 아키텍쳐를 제공하지 않고 Observable 과 같은 블록을 제공한다.

[👆](#table-of-contents)

### How to dispatch an action on load?

`componentDidMount()`와 `render()`메서드에서 데이터를 확인하는 액션을 전닥ㄹ할 수 있고 데이터를 확인할 수 있다.

```jsx harmony
class App extends Component {
  componentDidMount() {
    this.props.fetchData();
  }

  render() {
    return this.props.isLoaded ? (
      <div>{"Loaded"}</div>
    ) : (
      <div>{"Not Loaded"}</div>
    );
  }
}

const mapStateToProps = state => ({
  isLoaded: state.isLoaded
});

const mapDispatchToProps = { fetchData };

export default connect(
  mapStateToProps,
  mapDispatchToProps
)(App);
```

[👆](#table-of-contents)

### How to use `connect()` from React Redux?

container에서 store를 사용하기 위해서는 아래 두단계를 따라야 한다.

1. `mapStateToProps()`를 사용: state의 값을 props에서 지정한 store에 맵핑시킨다.
2. 위 props를 Container 와 연결: `mapStateToProps()`에 의해 리턴되는 객체들은 컨테이너와 연결된다. 이를 `react-redux`의 `connect`로 import 할 수 있다.

```jsx harmony
import React from "react";
import { connect } from "react-redux";

class App extends React.Component {
  render() {
    return <div>{this.props.containerData}</div>;
  }
}

function mapStateToProps(state) {
  return { containerData: state.data };
}

export default connect(mapStateToProps)(App);
```

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

```

```
