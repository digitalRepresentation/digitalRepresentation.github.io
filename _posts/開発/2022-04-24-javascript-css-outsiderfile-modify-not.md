---
layout: post
title: "javascriptやcssの外部ファイルが更新されない時に対処方法"
slug: javascript-css-outsider-file-modify
comments: true
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL"  width="700" height="370">
javascriptやcssの外部ファイルが更新されない時に対処方法    

## cssやjavascriptはどこで管理する方が良いか。
cssとjavascriptを学ぶ時は一つのhtmlファイルの中に使いますでしょうか。  
実は一つのhtmlファイルにcssとjavascriptを記載すると、最初は問題ありませんが、  
何回もメンテナンスをしてみたらかなりソースコードが複雑になる場合が多いです。  
その上で、一つの機能かデザインを他のページに使うときにも  
同じ内容を二つのhtmlに書くので可読性も良くないし、  
修正が入る場合に二つのHTMLファイルを修正しなければならないので、
ミスをしがちです。  

それでソースコードを組む場合はcssとjavascriptは<span style="color:red"><strong>外部ファイル</strong></span>として使う方が良いでしょう。  
メンテナンスもしやすくなりますし、開発工数も減ります。

## cssやjavascriptの外部ファイルの定義する方法は？

### css
cssは下記の文法を参考にしてくだいませ。  
hrefにファイルのパスとファイル名を書けば問題ないです。  

```html
<link rel="stylesheet" href="worldcupMainForm.css">
```

### javascript
javascriptは下記の文法を参考にしてくださいませ。  
srcにファイルのパスとファイル名を書けば問題ないです。  
```html
<script src="worldcupPlayerMethod.js"></script>
```

## cssやjavascriptの外部ファイルを使っても最新版にならない。
css、img、javascriptの外部ファイルを修正しても更新されない理由はブラウザのキャッシュクリアができないためです。  
一般的にブラウザをキャッシュするためにはCtrl+F5やブラウザの設定でキャッシュを削除するしかないです。  
しかし、ユーザー側は最新版になってない状態を知らないので、プログラミング上に修正するのが可能です。  
cssやjavascriptのファイルの後ろにハテナをつけて「?date=yyyymmdd」の形にすると、最新版となります。  
ハテナの後ろは日付を書いてもいいし、バージョン情報とかにも可能です。  
わかりやすく設定するのが可能なので、ファイルが最新にならないときは下記のやり方を使ってみてくださいませ。  

```html
<link rel="stylesheet" href="worldcupMainForm.css?date=20220424">
<script src="worldcupPlayerMethod.js?date=20220424"></script>
```

不明なところがありましたら、コメント欄に記載をお願いいたします。　　
