---
layout: post
title: "jekyllのブログがSearch Consoleのsitemapsが認識できない場合"
slug: sitemap-xml-console-search
comments: false
tags: [developer]
---
jekyllのブログがSearch Consoleのsitemapsが認識できない場合

## sitemap.xmlは何？
自分が作ったサイトに投稿した場合、世界で一番使われているGoogleに内容が表示されるのが遅いです。  
その時にgoogle search consoleツールを利用して新しい投稿されたのをURL検索してindexを作ります。  
そうすると、googleに素早に検索内容として表示されます。  
大量の投稿を管理するサイトはすごく面倒なのでsitemap.xmlを作っておくと、  
自動にindex作業を行います。  
  
## jekyllのブログがSearch Consoleのsitemapsが認識できない場合は
jekyllのブログでsitemap.xmlが基本的にありますが、  
google search consoleに登録したのに  
僕の場合は1年近い認識をしていませんでした。  
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
  
```xml
---
---
<?xml version="1.0" encoding="UTF-8"?>
    {% for post in site.posts %}
    <url>
        <loc>{{ site.url }}{{ post.url | remove: 'index.html' }}</loc>
    </url>
    {% endfor %}

    {% for page in site.pages %}
    {% if page.layout != nil %}
    {% if page.layout != 'feed' %}
    <url>
        <loc>{{ site.url }}{{ page.url | remove: 'index.html' }}</loc>
    </url>
    {% endif %}
    {% endif %}
    {% endfor %}
</urlset>
```


urlsetの内容を追加してください。    
```xml
<urlset xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9 http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd" xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
```


僕の場合は下記のようになります。

```xml
---
---
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.sitemaps.org/schemas/sitemap/0.9 http://www.sitemaps.org/schemas/sitemap/0.9/sitemap.xsd" xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    {% for post in site.posts %}
    <url>
        <loc>{{ site.url }}{{ post.url | remove: 'index.html' }}</loc>
    </url>
    {% endfor %}

    {% for page in site.pages %}
    {% if page.layout != nil %}
    {% if page.layout != 'feed' %}
    <url>
        <loc>{{ site.url }}{{ page.url | remove: 'index.html' }}</loc>
    </url>
    {% endif %}
    {% endif %}
    {% endfor %}
</urlset>
```


一ヶ月ぐらいでsitemap.xmlがgoogle search consoleに使えるようになりました。  
僕はgoogleアカウントが韓国語なので、下記のようになります。  
<img src="https://drive.google.com/uc?export=view&id=1sE2UzWQMjmQ21s8MOkldFuLv7_-R8v9L"  width="700"> 