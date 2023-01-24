---
layout: post
title: "htmlファイルでimgファイルがない時に別の画像ファイルにする方法"
slug: php-html-img-nophoto
comments: false
tags: [developer]
---
# htmlファイルでimgファイルがない時に別の画像ファイルにする方法
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="htmlファイルでimgファイルがない時に別の画像ファイルにする方法"  width="300" >
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
phpでhtmlのimgファイルがない時に代わりに別の画像が出る方法は二つあります。  
プログラミングってサーバーサイド言語のphpが動いた後、htmlが読み込まれるのを覚えてください。  

##　imgファイルがない場合別のファイルに変更する方法-phpを利用する。
if分岐でfile_existsというphpのファイル存在を確認してimgタグを吐き出す方法です。  
こちらをお勧めします。  
理由はphpで読み込む時にimgタグを決めますので、ブラウザー上に表示する際はスムーズに表示されます。  
```html
<?php if(file_exists( "/img/dev/one.jpg")): ?>
<img src="/img/dev/one.jpg">
<?php else: ?>
<img src="/img/dev/noPhoto.jpg" />
<?php endif; ?>
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
##　imgファイルがない場合別のファイルに変更する方法-htmlのonErrorを利用する。
imgの属性でonErrorがあります。  
imgのファイルがない時にonErrorを通してjsが実行されますので、ソースコードを書く時に綺麗に作成するのができます。  
こちらはブラウザー上で見ると、時間が少しかかります。  
なので、おすすめはしないです。  
```html
<img src="/img/dev/one.jpg" onerror="this.src='/img/dev/noPhoto.jpg';">
```
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7886659064712565"
     crossorigin="anonymous"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7886659064712565"
     data-ad-slot="1101493367"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
## htmlを動的に変えるのはSPAが良い。
Single Page ApplicationというSPAを使うと、  
作業コストもそんなにかからないし、速度も速いです。  
SPAだと、javascriptを基にしたVue.js、React.jsを使います。  