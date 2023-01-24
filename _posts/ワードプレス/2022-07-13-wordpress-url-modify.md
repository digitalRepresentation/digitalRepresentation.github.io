---
layout: post
title: "wordpressのurl変更する方法"
slug: wordpress-url-modify
comments: false
tags: [wordpress, developer]
---
## Wordpressのurl変更する方法を一分で紹介します。
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="wordpressのurl変更"  width="300" >
wordpressはブログをする時に必要なツールで一般的なサイトにもwordpressを導入する時は可能です。
ワードプレスを導入した時にバージョンファイルをダウンロードすると、`wp`フォルダがあってそれをルート内に格納します。
`wp`のままルート内に格納する場合はアドレスは下記となります。  
`https://digitalrepresentation.github.io/wp`  
こちらのアドレスで`wp`に接続する場合は他人からみてワードプレスを使うのもバレるし、あまり良くないです。    
例えば下記のように`wp`ではなく`blog`にワードプレスでurlを変更したい場合はどうすれば良いでしょうか。  
`https://digitalrepresentation.github.io/blog`  

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
  
## Wordpressにurlの変更する手順
`.htaccss`みたいなrouteの設定は不要です。  
1. ワードプレスの管理画面に移動してログインします。  
2. 左のメニューで「設定」を選択します。  
3. 「一般」のメニュを選択します。  
<img src="https://drive.google.com/uc?export=view&id=1bVdJrzr_er-M9CUAmGFcS18FRFH2LHgT" alt="wordpressのurl変更手順一番" >

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
  
4. WordPressアドレス(URL)、サイトアドレス(URL)を変更してください。  
※後ろに「/wp」だと書いてあるのでそれを「/blog」みたいな感じで修正してください。  
<img src="https://drive.google.com/uc?export=view&id=1A2U-SEc5S_eY27ob_O9vM8HT3Nq8fdml" alt="wordpressのurl変更手順二番" >

5. NOT FOUNDが出たらOKです。
6. プログラムのルート内にwpフォルダを変更したurlと同じく修正してください。  
7. 変わったurlの管理画面に接続できたら完了となります。  