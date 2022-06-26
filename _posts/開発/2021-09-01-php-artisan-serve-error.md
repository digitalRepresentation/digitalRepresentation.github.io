---
layout: post
title: "php-artisan-serve-errorエラーについて"
slug: php-artisan-serve-error
comments: true
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

# laravelでphp artisan serveを入力した際に下記のエラー解決
  

  
```php
$composer update
```
    
上記のコマンドを入力すると正常にできます。  