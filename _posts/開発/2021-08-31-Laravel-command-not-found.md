---
layout: post
title: "bash: laravel: command not foundエラーについて"
slug: laravel-command-not-found
comments: false
tags: [developer]
---
# bash: laravel: command not foundのエラーが発生する場合    

OS環境：MacOS  
laravel Version: laravel 8  

laravelでinstallをする場合、  
下記のコマンドができない時があります。  
  
```terminal
$laravel new project
bash: laravel: command not found
```
  
laravelを設定してもPATHを記載してなかったので下記の問題が発生します。  
  
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
  
# bash: laravel: command not foundのエラー解決
  

  
```php
$export PATH=$HOME/.composer/vendor/bin:$PATH
```
    
上記のようにlaravelのパスを設定すると問題解決です。  