---
title: "리액트 인터뷰 질문 & 답 (2)"
date: 2019-08-21 10:17:16
layout: post
tags: [javascript, react]
published: false
---

[목차](/2019/08/13/reactjs-interview-questions/)

## Table of Contents

| No. | Questions |
| --- | --------- |
|   | **React Router** |
|129| [What is React Router?](#what-is-react-router) |
|130| [How React Router is different from history library?](#how-react-router-is-different-from-history-library) |
|131| [What are the \<Router> components of React Router v4?](#what-are-the-router-components-of-react-router-v4) |
|132| [What is the purpose of push and replace methods of history?](#what-is-the-purpose-of-push-and-replace-methods-of-history) |
|133| [How do you programmatically navigate using React router v4?](#how-do-you-programmatically-navigate-using-react-router-v4) |
|134| [How to get query parameters in React Router v4](#how-to-get-query-parameters-in-react-router-v4) |
|135| [Why you get "Router may have only one child element" warning?](#why-you-get-router-may-have-only-one-child-element-warning) |
|136| [How to pass params to history.push method in React Router v4?](#how-to-pass-params-to-historypush-method-in-react-router-v4) |
|137| [How to implement default or NotFound page?](#how-to-implement-default-or-notfound-page) |
|138| [How to get history on React Router v4?](#how-to-get-history-on-react-router-v4) |
|139| [How to perform automatic redirect after login?](#how-to-perform-automatic-redirect-after-login) |
|   | **React Internationalization** |
|140| [What is React-Intl?](#what-is-react-intl) |
|141| [What are the main features of React Intl?](#what-are-the-main-features-of-react-intl) |
|142| [What are the two ways of formatting in React Intl?](#what-are-the-two-ways-of-formatting-in-react-intl) |
|143| [How to use FormattedMessage as placeholder using React Intl?](#how-to-use-formattedmessage-as-placeholder-using-react-intl) |
|144| [How to access current locale with React Intl](#how-to-access-current-locale-with-react-intl) |
|145| [How to format date using React Intl?](#how-to-format-date-using-react-intl) |
|   | **React Testing** |
|146| [What is Shallow Renderer in React testing?](#what-is-shallow-renderer-in-react-testing) |
|147| [What is TestRenderer package in React?](#what-is-testrenderer-package-in-react) |
|148| [What is the purpose of ReactTestUtils package?](#what-is-the-purpose-of-reacttestutils-package) |
|149| [What is Jest?](#what-is-jest) |
|150| [What are the advantages of Jest over Jasmine?](#what-are-the-advantages-of-jest-over-jasmine) |
|151| [Give a simple example of Jest test case](#give-a-simple-example-of-jest-test-case) |
|   | **React Redux** |
|152| [What is Flux?](#what-is-flux) |
|153| [What is Redux?](#what-is-redux) |
|154| [What are the core principles of Redux?](#what-are-the-core-principles-of-redux) |
|155| [What are the downsides of Redux compared to Flux?](#what-are-the-downsides-of-redux-compared-to-flux) |
|156| [What is the difference between mapStateToProps() and mapDispatchToProps()?](#what-is-the-difference-between-mapstatetoprops-and-mapdispatchtoprops) |
|157| [Can I dispatch an action in reducer?](#can-i-dispatch-an-action-in-reducer) |
|158| [How to access Redux store outside a component?](#how-to-access-redux-store-outside-a-component) |
|159| [What are the drawbacks of MVW pattern](#what-are-the-drawbacks-of-mvw-pattern) |
|160| [Are there any similarities between Redux and RxJS?](#are-there-any-similarities-between-redux-and-rxjs) |
|161| [How to dispatch an action on load?](#how-to-dispatch-an-action-on-load) |
|162| [How to use connect from React Redux?](#how-to-use-connect-from-react-redux) |
|163| [How to reset state in Redux?](#how-to-reset-state-in-redux) |
|164| [Whats the purpose of at symbol in the redux connect decorator?](#whats-the-purpose-of-at-symbol-in-the-redux-connect-decorator) |
|165| [What is the difference between React context and React Redux?](#what-is-the-difference-between-react-context-and-react-redux) |
|166| [Why are Redux state functions called reducers?](#why-are-redux-state-functions-called-reducers) |
|167| [How to make AJAX request in Redux?](#how-to-make-ajax-request-in-redux) |
|168| [Should I keep all component's state in Redux store?](#should-i-keep-all-components-state-in-redux-store) |
|169| [What is the proper way to access Redux store?](#what-is-the-proper-way-to-access-redux-store) |
|170| [What is the difference between component and container in React Redux?](#what-is-the-difference-between-component-and-container-in-react-redux) |
|171| [What is the purpose of the constants in Redux? ](#what-is-the-purpose-of-the-constants-in-redux) |
|172| [What are the different ways to write mapDispatchToProps()?](#what-are-the-different-ways-to-write-mapdispatchtoprops) |
|173| [What is the use of the ownProps parameter in mapStateToProps() and mapDispatchToProps()?](#what-is-the-use-of-the-ownprops-parameter-in-mapstatetoprops-and-mapdispatchtoprops) |
|174| [How to structure Redux top level directories?](#how-to-structure-redux-top-level-directories) |
|175| [What is redux-saga?](#what-is-redux-saga) |
|176| [What is the mental model of redux-saga?](#what-is-the-mental-model-of-redux-saga) |
|177| [What are the differences between call and put in redux-saga](#what-are-the-differences-between-call-and-put-in-redux-saga) |
|178| [What is Redux Thunk?](#what-is-redux-thunk) |
|179| [What are the differences between redux-saga and redux-thunk](#what-are-the-differences-between-redux-saga-and-redux-thunk) |
|180| [What is Redux DevTools?](#what-is-redux-devtools) |
|181| [What are the features of Redux DevTools?](#what-are-the-features-of-redux-devtools) |
|182| [What are Redux selectors and Why to use them?](#what-are-redux-selectors-and-why-to-use-them) |
|183| [What is Redux Form?](#what-is-redux-form) |
|184| [What are the main features of Redux Form?](#what-are-the-main-features-of-redux-form) |
|185| [How to add multiple middlewares to Redux?](#how-to-add-multiple-middlewares-to-redux) |
|186| [How to set initial state in Redux?](#how-to-set-initial-state-in-redux) |
|187| [How Relay is different from Redux?](#how-relay-is-different-from-redux) |
|   | **React Native** |
|188| [What is the difference between React Native and React?](#what-is-the-difference-between-react-native-and-react) |
|189| [How to test React Native apps?](#how-to-test-react-native-apps) |
|190| [How to do logging in React Native?](#how-to-do-logging-in-react-native) |
|191| [How to debug your React Native?](#how-to-debug-your-react-native) |
|   | **React supported libraries and Integration** |
|192| [What is reselect and how it works?](#what-is-reselect-and-how-it-works) |
|193| [What is Flow?](#what-is-flow) |
|194| [What is the difference between Flow and PropTypes?](#what-is-the-difference-between-flow-and-proptypes) |
|195| [How to use font-awesome icons in React?](#how-to-use-font-awesome-icons-in-react) |
|196| [What is React Dev Tools?](#what-is-react-dev-tools) |
|197| [Why is DevTools not loading in Chrome for local files?](#why-is-devtools-not-loading-in-chrome-for-local-files) |
|198| [How to use Polymer in React?](#how-to-use-polymer-in-react) |
|199| [What are the advantages of React over Vue.js?](#what-are-the-advantages-of-react-over-vuejs) |
|200| [What is the difference between React and Angular?](#what-is-the-difference-between-react-and-angular) |
|201| [Why React tab is not showing up in DevTools?](#why-react-tab-is-not-showing-up-in-devtools) |
|202| [What are styled components?](#what-are-styled-components) |
|203| [Give an example of Styled Components?](#give-an-example-of-styled-components) |
|204| [What is Relay?](#what-is-relay) |
|205| [How to use TypeScript in create-react-app application?](#how-to-use-typescript-in-create-react-app-application) |


[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
[👆](#table-of-contents)
