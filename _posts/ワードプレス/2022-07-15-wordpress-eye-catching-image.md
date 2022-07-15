---
layout: post
title: "アイキャッチ画像が表示されない場合ワードプレス解決方法"
slug: wordpress-eye-catching-image
comments: false
tags: [wordpress, developer]
---
## アイキャッチ画像が表示されない場合ワードプレス解決方法
<img src="https://drive.google.com/uc?export=view&id=1v1g06Mvx-zclnrCYaiONnnaPSZV-wswx" alt="wordpressのエラー"  width="500" >
ワードプレスで管理画面からサムネイルを追加しようと思ったら、アイキャッチ画像がない場合はございませんか。  
実は管理画面のオプションにアイキャッチ画像が表示されないと出ている時があります。  
この場合は記載するメニューの隣の表示オプションを押します。    
<img src="https://drive.google.com/uc?export=view&id=1yaWEj9YjMfVIX_AMIs_D3wdop53z3KQ8" alt="wordpressのエラー2"  width="500" >
クリックしたらアイキャッチ画像があって選択すれば解決できます。
しかし、表示オプションを選択しても下記のようにアイキャッチ画像がない場合があります。  
それについて解決できる方法を説明します。  
<img src="https://drive.google.com/uc?export=view&id=1r1CAONTqEvWPp-X8u8tsSvoTAX9jEzec" alt="wordpressのエラー3">

## ワードプレスの表示オプションにアイキャッチ画像がない場合の解決方法
簡単にphpファイルを修正すれば問題ありません。  
function.phpファイルの一番下に下記の内容を登録してください。  
`wp-content/themes/使っているテーマ/function.php`  
```php
add_theme_support('post-thumbnails');
```
追加した後で管理画面に戻って表示オプションをもう一度クリックすると、  
アイキャッチ画像があるのでそれを選択すれば解決できます。  
<img src="https://drive.google.com/uc?export=view&id=1lvQOyM3dwEGx5y1VlrkI208NRpv_HFAK" alt="wordpressのエラー4">

## phpファイルにアイキャッチ画像を使う方法
phpファイルでアイキャッチ画像を呼び出してリストページで使いたい人もいると思います。  
その時は下記のように`the_post_thumbnail()`関数を使ってください。  
```php
<?php if(have_posts()): while(have_posts()):the_post(); ?>
<?php echo the_post_thumbnail('thumbnail'); ?>
<?php endif; ?>
```