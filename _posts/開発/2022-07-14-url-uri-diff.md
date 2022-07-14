---
layout: post
title: "URLとURIの違い"
slug: url-uri-diff
comments: false
tags: [developer]
---
## URLとURIの違い
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="uriとurlの違い"  width="300" >
一般的にサイトのパスを呼ぶ時はURLを使っていませんか。  
URL(Uniform Resource Locator)は全てのホームページのパスを指名するのではありません。
IT業界も主に使われる用語ですし、間違えて使っている人が多いでしょう。
ネット環境でリソースを識別する時はPath Variable方式と Query Parameter方式があります。  
ここでリソースはWebで連携されるものだと認識すれば良いです。  

## URLとは
URL(Uniform Resource Locator)は下記のような仕組みです。  
URLはWEBでアクセス可能なリソース(資源)の住所を一貫的に表現する方式です。  

```html
https://digitalrepresentation.github.io/search/1
https://digitalrepresentation.github.io/search/2
https://digitalrepresentation.github.io/search/3
```

## URIとは
URI(Uniform Resource Identifier)はリソースの位置だけではなく、IdentifierとしてURLを含まれています。  
いわゆるGETの方式で使われる住所はURIです。  

```html
https://digitalrepresentation.github.io/search?type=ghost
https://digitalrepresentation.github.io/search?type=terran
https://digitalrepresentation.github.io/search?type=game
```

## URLとURIは何が違うか
URIはURLの内容も含まれています。なのでURIの範囲の内にURLがあります。  
下記の画像をご覧ください。  
Query Stringが入っていたらURIで、Query StringがなくてPathまである場合はURLだと認識すれば問題ないです。  

<img src="https://drive.google.com/uc?export=view&id=1xXgMJNUvBlYQ0dXCiSoj82Wtshp0wZfN" alt="uriとurlの違い2">