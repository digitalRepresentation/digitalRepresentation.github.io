---
layout: post
title: "php-artisan-serve-errorエラーについて"
slug: php-artisan-serve-error
comments: false
tags: [developer]
---
# laravelでphp artisan serveを入力した際に下記のエラーが発生する場合    

OS環境：MacOS  
laravel Version: laravel 8  

laravelでphp artisan serveを入力した際に下記のエラーが発生しました！  
  
```terminal
$php artisan serve
Warning: require(/Users/jinyoungkim/recipe-osusume/recipe-osusume/recipe-osusume/vendor/autoload.php): failed to open stream: No such file or directory in /Users/jinyoungkim/recipe-osusume/recipe-osusume/recipe-osusume/artisan on line 18

Fatal error: require(): Failed opening required '/Users/jinyoungkim/recipe-osusume/recipe-osusume/recipe-osusume/vendor/autoload.php' (include_path='.:/usr/local/Cellar/php@7.4/7.4.23/share/php@7.4/pear') in /Users/jinyoungkim/recipe-osusume/recipe-osusume/recipe-osusume/artisan on line 18
```
  
projectのcomposer updateがされてない時、上記のエラーが発生します。  

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
　　
# laravelでphp artisan serveを入力した際に下記のエラー解決
  

  
```php
$composer update
```
    
上記のコマンドを入力すると正常にできます。  