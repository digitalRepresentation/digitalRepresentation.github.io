---
layout: post
title: "phpメンバ変数に「$_SERVER」が叩かない場合は"
slug: php-class-variable-server
comments: false
tags: [developer]
---
phpメンバ変数に「$_SERVER」が叩かない場合は  

## phpの$_SERVERとは
phpの内蔵配列で、urlの情報を持っている配列です。  

## class内に$_SERVERができない
classは$_SERVERより早く読み込まれるので、  
最初の変数に入れて使うのは不可です。  
実行してみると真っ白くなります。  
```php
class test {
    const SERVER_URL = $_SERVER;
}

$testObj = new Test();
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
  
## class内に$_SERVERが使える方法は？
constructにメンバ変数の値を指定すれば問題解決です。  
classは$_SERVERより先に作られますので、  
最初に$_SERVERを持つのが不可能ですが、constructでClassをインスタンスすれば問題ないです。  
constは定数なので、今回は普通の変数を使いました。  

```php
class test {
    private $serverUrl;

    function __construct() {
        $this->serverUrl = $_SERVER;
    }
}
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
  
$testObj = new Test();
```

