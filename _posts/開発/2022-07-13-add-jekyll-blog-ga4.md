---
layout: post
title: "jekyllのブログでgoogle analytics GA4導入する"
slug: add-jekyll-blog-ga4
comments: false
tags: [developer]
---
## jekyllのブログでgoogle analytics GA4導入する
<img src="https://drive.google.com/uc?export=view&id=11PGGZrXOSYSkbMxiM-p1vwqZoOxan8wR" alt="jekyllでgoogle analytics" width="700">
jekyllのブログを使う時にgoogle analyticsを導入する方法がわからない人が多いです。  
｀_config.yml`のファイルを開いて下記の内容を確認します。  
```yml
#google_analytics:      UA-XXXXXXX-X  #NG
#google_analytics:      G-XXXXXXX  #OK
```
`UA-XXXXXXX-X`書いてある場合はuniversal analyticsで古いバージョンです。  
昔からjekyllでブログを作った時はGA4が出る前だったので、UAになっている可能性が高いです。  
この場合は直で貼り付けます。下に記載しているので下を確認してください。  
`G-XXXXXXX`はGA4のIDとなります。こちらの場合は注釈を削除してIDを貼り付けば起動できます。  
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
  
## jekyllの_configファイルにGoogle Analytics GA4が対応できない場合に対策方法
Google Analytics ScriptはHTMLの`<html>`内部に入れます。
それでブログルートの`_includes`に移動してヘッダー部分を担当しているファイルを探して該当するファイルにScriptを入れる流れになります。  
下記の画像の通りに移動してください。  
1. 左下の設定マークをクリックします。  
2. データストリームをクリックします。  
3. アカウントを作った時に生成したストリームをクリックする。（ストリームがなかったらストリーム追加で作成すれば良いです。）    
    
<img src="https://drive.google.com/uc?export=view&id=12sT_B0E7xMfAdgMr0jUXIAqH4XHAyAks" alt="jekyllでgoogle analytics2">
    
4. タグ設定手順の下に新しいページ状のタグを追加するをクリックします。  
5. グローバル サイトタグ（gtag.js） ウェブサイト作成ツールや、CMS でホストされるサイトをご使用の場合、このタグを設定をクリックします。  

<img src="https://drive.google.com/uc?export=view&id=1GUDRiy1unNy2_wzY8rhytKXD9QHu0MMX" alt="jekyllでgoogle analytics3">
    

6. ブログフォルダの`_include`に移動してヘッダーを担当するファイルを探して上記のGA Scriptを挿入します。jekyllのテーマによってファイルの構成が違いますが、私の場合は`my-head.html`にGA Scriptを挿入しました。あるテーマの場合は`analytics.html`ヘッダーを担当しているのでそのファイルを修正する場合もあります。  
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
  
## Google Analytics4が導入できたのか確認する方法
ブラウザの`コンソール`を開いてgtagを叩いてみます。  
### GA4の導入が失敗した場合
<img src="https://drive.google.com/uc?export=view&id=1N2CVGmg7gtuHZA8ItkQULbHhdWcQEuwh" alt="jekyllでgoogle analytics4">
### GA4が成功的に導入した場合
<img src="https://drive.google.com/uc?export=view&id=1R-OoO6KGl8fbaDCU_PPOD9N6bAI7ANM1" alt="jekyllでgoogle analytics5">

失敗した場合はページのソースコードを見てGAストリームIDが正しいのか、`head`内にG-XXXXXXがあるのか確認する必要があります。大体誤字で対応できてない場合が多いので修正してやってみてください。  