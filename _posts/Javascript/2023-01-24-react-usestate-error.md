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
    
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7886659064712565"
     crossorigin="anonymous"></script>
<!-- 디스플레이 광고 -->
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7886659064712565"
     data-ad-slot="1939383573"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
  

##　'useState'を呼び出す
useStateを呼び出す時はimport Reactに下記の構文を作成すれば解決できます。  
```javascript
import React, { useState } from 'react';
```