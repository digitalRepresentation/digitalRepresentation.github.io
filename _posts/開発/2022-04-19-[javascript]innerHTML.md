---
layout: post
title: "[javascript]innerHTMLでHTMLコードを追加してみよう"
slug: phpmyadmin-loginform
comments: true
tags: [developer]
---
  
## innerHTMLでHTMLコードを追加してみよう

javascriptはinnerHTMLという機能で簡単にHTML内容を追加するのが可能です。  
基本的には記載した内容があってもクリアされてあらためて作成される形となります。

```html
<p id='ptag'>
    innerHTMLを使いましょう。
</p>
```

```javascript
let ptagId =  document.getElementById('ptag');
ptagId.innerHTML = "<a>innerHTMLを使いましょう</a>";
```

### 結果
```html
<p id='ptag'>
    <a>innerHTMLを使いましょう</a>
</p>
```

もちろん、innerHTMLで既存のHTMLが削除されてなくて追加するのも可能です。  
2ヶ所ありますので、ご覧くださいませ。  

## 1. innerHTMLで追加します。

下記の書き方にすれば大丈夫です。  

```html
<p id='ptag'>
    innerHTMLでどうやって既存のHTMLを残してinnerHTMLが出力できるの？
</p>
```

```javascript
let ptagId =  document.getElementById('ptag');
ptagId.innerHTML += "<a>このやり方で可能です。</a>";
```

### 結果
```html
<p id='ptag'>
    innerHTMLでどうやって既存のHTMLを残してinnerHTMLが出力できるの？
    <a>このやり方で可能です。</a>
</p>
```

既存のHTMLの上に配置されて追加するのは可能です！  
しかし、既存のHTMLの上にするのはどうすれば良いでしょうか。

## 2. insertAdjacentHTML関数を使いましょう！
insertAdjacentHTMLを使用すると、タグの周りにセットするのが可能です！ 

```html
<!-- beforebegin -->
<p id='ptag'>
<!-- afterbegin -->
    insertAdjacentHTMLを使いましょう。
<!-- beforeend -->
</p>
<!-- afterend -->
```

innerHTMLで使うときはbeforeendに配置するので他のところにタグを置きたい際は  
insertAdjacentHTMLを使えば問題ないです。  

使い方は下記の通りです。  
```javascript
let ptagId =  document.getElementById('ptag');
ptagId.nsertAdjacentHTML('afterbegin', '<a>結果</a>');
```

### 結果
```html
<p id='ptag'>
<a>結果</a>
    insertAdjacentHTMLを使いましょう。
</p>
```
簡単にできましたか。  
速度はinnerHTMLが早いです。  
なので、用途に合わせて使ってくださいませ。  