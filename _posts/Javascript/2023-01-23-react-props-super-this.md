---
layout: post
title: "Must call super constructor in derived class before accessing 'this' or returning from derived constructorエラー解決"
slug: react-props-super-this
comments: false
tags: [javascript, developer]
---
# Must call super constructor in derived class before accessing 'this' or returning from derived constructorエラー解決
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Must call super constructor in derived class before accessing 'this' or returning from derived constructorエラー解決" width="600">
ESLintは'this' is not allowed before 'super()'というエラーを吐き出す場合があります。  
これはclassのstateコンポーネントを使う時に発生するエラーです。  
constructor(props)の処理を入れた時にreactのコンポーネントはComponentのClassを参照しているので、  
super(props)を書かなければなりません。

```javascript
import React, { Component } from 'react';

class DDayCounter extends Component {
    constructor(props) {
        super(props);
    }
}

export default DDayCounter;
```

constructor(props)を作成する場合は親のsuperを呼ぶ習慣をつけましょう。