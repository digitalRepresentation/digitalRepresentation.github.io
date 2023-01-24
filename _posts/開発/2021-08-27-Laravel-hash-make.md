---
layout: post
title: "Laravel hash::makeを使用してみた。"
slug: Laravel-hash-make
comments: false
tags: [developer]
---
# laravelでパスワードを暗号化して      

laravelはパスワードを暗号化が可能です。    
下記のように使われます。  
  
```php
Hash::make($変数名);
```

普段パスワードを暗号化するために使用されています。  
$変数名は同じ値を入れても毎回別の値を付与されます。  
では、どういうふうにすれば暗号化されたパスワードをチェックするのが可能でしょうか！  
DBの上は暗号化されているので呼び出す際は必ず<span style="color:red"><strong>暗号化になっている内容をチェックする関数を利用</strong></span>していきます。  

どういうことかと下記の内容をご覧ください。  
  
```php
// usersのテーブルでカラム名がusersの値に入力側Formの$userの値を入れて、passwordの値を検索する意味です。
// user名がある場合、hashされているパスワード値を持ってきます。
// user名がない場合、nullをreturnします。
$DBのパスワード値 = DB::table('users')->where('user', $user)->value('password');
hash::check($入力側Formの値, $DBのパスワード値);
```
  
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
  
「hash::check」というLaravelの関数を利用してパスワードが一致しているのか確認ができます。  
なので、$入力側Formの値が123456なら$DBのパスワード値は$2y$10$BiK3Shkz2sXfVOuvAQjr0ehZeSqg.P0y.WUk4Lq6WsRBQ4hspccJGみたいな値を持っていて  
内蔵関数を利用してチェックをする機能です。  

## 終わりに
Laravelの関数を利用して安全性が高いデータ暗号化が可能となります。