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

# bash: laravel: command not foundのエラー解決
  

  
```php
$export PATH=$HOME/.composer/vendor/bin:$PATH
```
    
上記のようにlaravelのパスを設定すると問題解決です。  