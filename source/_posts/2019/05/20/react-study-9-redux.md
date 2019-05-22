---
title: "React 공부하기 9 - Redux"
date: 2019-05-20 19:08:10
layout: post
tags: [react, javascript]
published: false
---

## Redux

컴포넌트 수가 많아지게 되면 상태관리하는 로직이 엄청나게 복잡해지고 관리도 까다로워 질 수 밖에 없다. 그래서 쓰는 것이 리덕스다. 리덕스는 상태 관리 로직을 컴포넌트 밖에서 처리하게 하는 것이다. 리덕스를 사용하면 모든 상태 관리가 스토어에서 발생하게 된다. 상태에 어떤 변화가 필요할 때는 `action`을 스토어에 전달한다. 액션은 객체 형태로 되어 있으며, 상태를 변화시킬 때 이 객체를 참조하여 변화를 만든다. 액션을 전ㄷ라하는 과정을 `dispatch`라고 한다. 스토어가 액션을 받으면 `reducer`가 전달받은 액션을 기준으로, 어떤식으로 상태를 변경시킬지 결정한다. 스토어 내부에 상태가 바뀌면, 스토어를 구독하고 있는 컴포넌트에 해당 값을 전달한다. 이 떄 부모 컴포넌트에 값을 넘기는 작업은 생략하고, 리덕스에서는 바로 컴포넌트를 스토어에 구독시킨다.

- 스토어: 어플리케이션의 상태 값들을 내장
- 액션: 상태 변화를 일으킬 때 참조하는 객체
- 디스패치: 액션을 스토어에 전달하는 것
- 리듀서: 상태를 변화시키는 로직이 있는 함수
- 구독: 스토어 값이 필요한 컴포넌트는 스토어의 상태를 subscribe


<!-- ### Action -->

<!-- 
{% raw %}
<a class="jsbin-embed" href="http://jsbin.com/bifagucexu/embed?html,js,console">test on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?4.1.7"></script>
{% endraw %} 
-->
