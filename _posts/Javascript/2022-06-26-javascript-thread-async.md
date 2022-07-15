---
layout: post
title: "javascriptのシングルスレッドなのに非同期になる理由を解説します。"
slug: javascript-シングルスレッド-非同期になる-理由-解説
comments: false
tags: [javascript, developer]
---
# javascriptのシングルスレッドなのに非同期になる理由を解説します。
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="javascript スレッド" width="700">
シングルスレッドとは一つのプログラムで一つのコードを実行されると言う意味です。  
javascriptはシングルスレッド言語です。  
C#, JAVA, rubyはマルチスレッド言語ですが、javascriptもシングルスレッドなのに非同期が可能です。    
非同期（Asynchrous)とは先に実行されるコードの作業が終わる前に後で実行されるコードの作業が終われることを意味します。  
つまり、同時に動けるコードを意味します。  
ジャバスクリプトのV8エンジンは`シングルスレッド`を持っているので、一つのstackしかありません。  
果たしてjavascriptは`シングルスレッド`なのにどうやって非同期的に実行ができるでしょうか。  

## ブラウザの中にWEB APIがあるのでjavascriptで非同期的な処理が可能です。
ブラウザは`dom`、`ajax`、`timeout`等 event loopとqueを持っています。　　
ブラウザで非同期ができる理由はWEB APIを提供しているからです。  
```typescript
console.log('実行１');
setTimeout(function asyncTest() {
	console.log('実行２');
}, 3000);
console.log('実行３');
```
こちらの結果はどうなると思いますか？  
シングルスレッドなら、下記のようになります。  
実行１→実行２→実行３  
しかしブラウザ上は下記のようになります。
実行１→実行３→実行２  
setTimeoutはブラウザーで提供するAPIです。Javascriptが実行されるruntime環境とは別であるエリアです。  
setTimeoutの呼び出しはstackからしますが、ブラウザーがタイマーを実行してカウントされるのは別のエリアです。  

## Eventloop
javascript非同期の概念で大事になるのはイベントループです。  
javascriptはStackを持っていますが、Stackが全部亡くなる時にQueをStackに移動することができます。  
なので、WEB APIで非同期を持っていて、CallBackを使う時に処理がQueに移動をして、  
Javascript処理が終わった時点(stackが全てない状態)に、callback関数が処理されます。  