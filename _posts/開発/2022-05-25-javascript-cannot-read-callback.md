---
layout: post
title: "Cannot read properties of null (reading 'addEventListener')のエラー対応"
slug: javascript-cannot-read-callback
comments: false
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL"  width="700">
Cannot read properties of null (reading 'addEventListener')のエラー対応    

## エラー内容の意味
外部のjsファイルを呼ぶ時に下記のエラーになることがあります。　　
Cannot read properties of null (reading 'addEventListener')　　
英語の意味の通りにaddEventListenerを使えないと出ています。  
なんでこのエラーになるでしょうか。  

## エラー原因
本件のエラーはjsが最初に読み込んで、その中にHTML DOMを呼ぶので、
DOMの情報がないので上記のエラーになります。　　
なので、DOMのIDかCLASSがないのにjsが先に実行してしまい、本件のエラーになりますね。  

## エラー解決
本件は三つの解決方法があります。  

### 一番目　bodyタグの一番下に記載します。
bodyの情報がレンダリングできた後に一番下に記載します。  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>例問題</h1>
    <div id="test"></div>
    <script type="text/javascript" src="include.js"></script>
</body>
</html>
```


### 二番目　javascriptのdeferを使います。
javascriptでdefer属性があります。  
headの方に記載してもbodyが全部レンダリングした後にjsファイルを呼び出します。  
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script type="text/javascript" src="include.js" defer></script>
    <title>Document</title>
</head>
<body>
    <h1>例問題</h1>
    <div id="test"></div>
</body>
</html>
```

### まとめ
使い方もいろいろあって開発者によって違います。
headにjsファイルがいっぱいあったら可読性がよくないので、  
bodyの中に一番下に記載するのも良いやり方かと思います。  