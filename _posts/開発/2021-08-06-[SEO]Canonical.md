---
layout: post
title: "Canonicalタグとは"
slug: Canoicalとは
comments: true
tags: [developer]
---
  
## Canonical(カノニカル)とは


canonicalとは直訳すると“標準的な”といった意味で、冒頭でもご説明したように、複数アクセスできてしまうurlの中から標準的なurlを指定する「urlの正規化」を意味します。

カノニカルタグは<span style="color:red">サイトの内にURLは違うが、同じ内容の重複となっているページがある場合、
ページにコードを挿入して検索エンジンに代表となるURL役割を教えてくれる役割のタグ</span>です。  

例えば、下記のように同じページですが、パラメータの値があったり、データを分析するため、コードを挿入した場合、  
実は同一なページに連携されているが、URLは違う場合があります。  
しかし、検索エンジンは下記のコンテンツが類似なページだと認識してしまい、  
同じページを違うページだと認識されてしまいます。  

    https://digitalrepresentation.github.io/blog_search
    https://digitalrepresentation.github.io/blog_search?name=nomura
    https://digitalrepresentation.github.io/blog_search?utm_campaign=event


## カノニカル(Canonical)tagを適用しないとどうなるのでしょうか。

### １。SubのページがMainになってしまいクローリングなる可能性がある。
<strong>https://digitalrepresentation.github.io/blog_search</strong>をメインだと認識してしまい、
メイン以外のページのクローリングを少なくする可能性があります。

### ２。検索エンジンにペナルティーをもらう可能性がある。
同じページが各々のurlに分散されている場合、  
集客が多いと思うのですが、実は一つのURLより集客率が低くなります。


## カノニカル(Canonical)tagの使用方法は何でしょうか。

下記のようにメインのurlを指定してつけたら大丈夫です。
htmlのheadタグの中に入ります。

```html
<head>
   <link rel="canonical" href="https://digitalrepresentation.github.io/blog_search">
</head>
```


## SEO対策をして利益をあげていきましょう！