---
layout: post
title: "Javascriptの「Reduce of empty array with no initial value」エラー解決方法"
slug: javascript-reduce-initial-value-error
comments: false
tags: [developer]
---
## Javascriptの「Reduce of empty array with no initial value」エラー対応方法
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Reduce of empty array with no initial value解決" width="300">
javascriptのreduceを使用する時にエラーがなる場合「Uncaught TypeError: Reduce of empty array with no initial value」になることがありますでしょう。
```javascript
const sum = [].reduce((x, y) => x + y);
```

## Reduce of empty array with no initial valueエラー解決方法
JavascriptのReduceメソッドはArrayで使われるメソッドです。  
エラーになる理由はreduceを使う配列が空の場合はエラーになります。  
この場合はreduceの二つ目の引数が初期値です。  
javascriptのreduceを使う時は必ず初期値を設定する必要があります。  
```javascript
const sum = [].reduce((x, y) => x + y, 0);
```