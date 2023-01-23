---
layout: post
title: "ESLintのParsing error: Unexpected token, expected ','エラー解決"
slug: eslint-parsing-error-komma
comments: false
tags: [javascript, developer]
---
# ESLintのParsing error: Unexpected token, expected ","エラー解決
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Parsing error: Unexpected token, expected ','エラー解決" width="600">
ESLintのエラーParsing error: Unexpected token, expected ","が発生しました。  
こちらはjavascriptのObjectの中に最後コンマをつけてなくて、セミコロンを使ってしまい、エラーになると思います。  
下記のソースコードをご覧ください。  

## ESLintのParsing error: Unexpected token, expected ","エラー例
Reactのコンポーネントですが、return {dDayNumber : dDayNumber + 1;}にエラーがなりました。  

```javascript
import React, { Component } from 'react';

class DDayCounter extends Component {
    constructor(props) {
        super(props);
    }

     render() {
        const { dDayNumber } = this.state;
        return (
            <div>
              <button onClick={() => {
                this.setState(prevState => {
                  return {dDayNumber : dDayNumber + 1;}
                });
              }}
              >増加</button>
            </div>
        );
    }
}

export default DDayCounter;
```
  
## ESLintのParsing error: Unexpected token, expected ","エラー解決方法
javascript objectはコンマで分岐するのでセミコロンではなく、コンマに修正をしてください。  

```javascript
import React, { Component } from 'react';

class DDayCounter extends Component {
    constructor(props) {
        super(props);
    }

     render() {
        const { dDayNumber } = this.state;
        return (
            <div>
              <button onClick={() => {
                this.setState(prevState => {
                  return {dDayNumber : dDayNumber + 1,}
                });
              }}
              >増加</button>
            </div>
        );
    }
}

export default DDayCounter;
```