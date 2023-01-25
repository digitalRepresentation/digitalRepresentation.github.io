---
layout: post
title: "VSCodeで必要なReactのパッケージを紹介します。"
slug: vscode-reactjs-code-snippets
comments: false
tags: [javascript, developer]
---
# VSCodeで必要なReactのパッケージを紹介します。
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="vscode-reactjs-code-snippets" width="600">

Reactを設置して使う時にVisual Studio Codeのツールでパッケージを入れないと、  
メモ帳とあまり変わらないです。  

## 「Reactjs Code Snippets」のVsCode Packageを入れて使いましょう。  
Reactjs Code Snippetsを使うと作業時に時間がかなり減ります。  
Reactの文法を作成する時、割と時間がかかるし、ミスをしてしまったらもっと無駄な時間がかかります。  
しかし、パッケージを使うとこういう問題を解決するのができます。  
  
パッケージを設置後に新しいjsファイルを作ってくださいませ。  
その後に、rccと入力してTabキーを押してください。　　
```javascript
rcc
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
  
すると、ファイル名に合わせて、react class形でコンポーネント作成するのが可能です。
```javascript
import React, { Component } from 'react';

class Counter extends Component {
    render() {
        return (
            <div>
                
            </div>
        );
    }
}

export default Counter;
```

他も自動で作るパタンがありますので、公式ホームページに入って確認してみてください。  
[https://marketplace.visualstudio.com/items?itemName=xabikos.ReactSnippets](https://marketplace.visualstudio.com/items?itemName=xabikos.ReactSnippets)  