---
layout: post
title: "MACOS環境にphpmyadminのloginformが出ない場合、解決方法"
slug: phpmyadmin-loginform
comments: false
tags: [developer]
---
  
## MACOS環境にphpmyadminを構築しましたが、loginformがでてない。

phpmyadminに別のアカウントをログインしたいですが、  
<span style="color:red">ログアウトしてもログインフォームに戻れない問題</span>が発生しました。  
原因はphpmyadminの設定がうまく行けない場合がございます。  

## MACOS環境でphpmyadminの設定ファイルはどこにある？

phpmyadminの設定ファイル名は<span style="color:red">config.inc.php</span>のファイルです。  
MACOSの場合はそのファイルがどこにあるのかわからない場合が多いです。  
ファイルのパス情報を探したいときは下記のコメントをterminalに入力してくださいませ。  
```shell
% sudo find / -iname "config.inc.php"
```

## config.inc.phpがreadonlyになっていて修正ができない場合は？

viモードでファイルを修正する場合、readonlyになってしまい  
修正ができない場合があります。  
ファイルの権限を修正してもできなかった場合は下記のコメントを入力してくださいませ。  
```shell
% sudo nano config.inc.php
```

## config.inc.phpの内を修正すればログインフォームを出力できるのか？

config.inc.phpの中身を閲覧してauto_typeをconfig→cookieに修正してくださいませ。

```php
$cfg['Servers'][$i]['auth_type'] = 'config'; 
```

```php
$cfg['Servers'][$i]['auth_type'] = 'cookie'; 
```

最後にapache, mysql serverを再起動するとうまくいけます。
何か不明点がありましたらコメントをお願いいたします。