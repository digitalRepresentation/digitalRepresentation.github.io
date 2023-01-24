---
layout: post
title: "JSLintの'useState' is not defined.のエラー対応方法"
slug: react-usestate-error
comments: false
tags: [javascript, developer]
---
# JSLintの'useState' is not defined.のエラー対応方法エラー
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="JSLintの'useState' is not defined.のエラー対応方法" width="600">
ReactでuseStateを使う時に存在してない関数だとエラーが発生した時があります。  


```javascript
import React from 'react';

const Test = () => {
  const [userName, setUserName] = useState('');
    return (
        <div>
            
        </div>
    );
};

export default Test;
```
    
<p class="hr">

##　'useState'を呼び出す
useStateを呼び出す時はimport Reactに下記の構文を作成すれば解決できます。  
```javascript
import React, { useState } from 'react';
```