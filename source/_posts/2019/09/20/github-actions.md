---
title: "github actions 사용해보기"
date: 2019-09-20 09:18:09
layout: post
tags: [github]
---

## Github actions로 hexo 블로그 배포하기

잘될까?

`/.github/workflows/nodejs.yml`

```yaml
name: Node CI

on:
  push:
    branches:
      - master

jobs:
  build:
    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [8.x, 10.x, 12.x]

    steps:
      - uses: actions/checkout@v1
      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v1
        with:
          node-version: ${{ matrix.node-version }}
      - name: deploy blog
        run: |
          npm ci
          npm run deploy
        env:
          CI: true
```

github이 아닌 로컬에서 빌드를 수정하고 푸쉬하는건 허용되지 않는 것 같다.
