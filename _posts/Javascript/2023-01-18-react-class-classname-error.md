---
layout: post
title: "Invalid DOM property `class`. Did you mean `className`エラー解決"
slug: react-class-classname-error
comments: false
tags: [javascript, developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Invalid DOM property `class`. Did you mean `className`" width="700">

## 「Invalid　DOM property `class`. Did you mean `className`」エラー解決方法
React v16バージョン以降からはclassを使用しても挙動は問題ありませんが、  
コンソールはエラーを吐き出します。  
  
エラーになるソースコード  
```css
.title {
  height: 40vmin;
  pointer-events: none;
}
```
```javascript
  return <div class="title">水曜日夜は勉強する時間となります。</div>
```

## 「Invalid　DOM property `class`. Did you mean `className`」エラーを出さないように修正しました。
classをclassNameに変更すればConsoleで上記のエラー問題を解決するのができます。  
```css
.title {
  height: 40vmin;
  pointer-events: none;
}
```
```javascript
  return <div className="title">水曜日夜は勉強する時間となります。</div>
```