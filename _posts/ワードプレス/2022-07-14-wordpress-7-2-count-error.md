---
layout: post
title: "Parameter must be an array or an object that implements Countable in"
slug: wordpress-7-2-count-error
comments: false
tags: [wordpress, developer]
---
## Parameter must be an array or an object that implements Countable in <b>wp/wp-includes/post-template.php</b> on line <b>284</b><br />のエラーの解説 Wordpress
<img src="https://drive.google.com/uc?export=view&id=1v1g06Mvx-zclnrCYaiONnnaPSZV-wswx" alt="wordpressのエラー"  width="500" >
ワードプレスの下記のエラーを見たことがありますでしょうか。  
Parameter must be an array or an object that implements Countable in <b>wp/wp-includes/post-template.php</b> on line <b>284</b><br />のエラーの解説 
このエラーはワードプレスでphp7.2のバージョンを使う時になります。  
`get_the_excerpt()`を使うと上記のエラーになるので困ってはありませんか。  

wpフォルダのwp-includesのpost-template.phpの284行目を下記のように変更してください！  
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
  
```php
if ( is_array($pages) ) {
    if ( $page > count( $pages ) ) // if the requested page doesn't exist
    $page = count( $pages ); // give them the highest numbered page that DOES exist
}
```

こちらの問題がなるのはphp7.2以上のバージョンでcountの使い方が変わったからです。  
詳しい内容は下記のドキュメントを参考にしてくださいませ。  
[php-Document-count()](https://www.php.net/manual/ja/function.count.php)
