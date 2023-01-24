---
layout: post
title: "「www.youtube.comで接続が拒否されました。」のエラー対策"
slug: youtube-iframe-error
comments: false
tags: [developer]
---

<img src="https://drive.google.com/uc?export=view&id=11PGGZrXOSYSkbMxiM-p1vwqZoOxan8wR" alt="youtube error"  width="700">

# 「www.youtube.com で接続が拒否されました。」のエラー対策
youtubeの動画をiframeのsrcで挿入する際に、www.youtube.comで接続が拒否されました。というエラーが出ました。 
エラーはurlの描き間違えです。  
このままurlを入れるとiframeで読み込まれないです。  

<img src="https://drive.google.com/uc?export=view&id=1atPJmnA7V6dolOLwA5DLUZQx8To5y08B" width="500" alt="www.youtube.comで接続が拒否されました。">
  
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
  
なので下記のurlみたいにshortsをembedに変更すれば問題解決となります。  
修正前：www.youtube.com/<span style="color:red; font-weight: bold;">shorts</span>/c3UIJLv-bzs  
修正後：www.youtube.com/<span style="color:red; font-weight: bold;">embed</span>/c3UIJLv-bzs  

<img src="https://drive.google.com/uc?export=view&id=1trmBl-Do9JLcqCq1c6OrsJaMW78gbJtO"  width="700" alt="www.youtube.comで接続が拒否">

## 「www.youtube.com で接続が拒否されました。」解決
下記のようにshortsをembedに修正すると、  
動画が表示されます。  

<img src="https://drive.google.com/uc?export=view&id=1UDyBVNWaxcFJpPmSNUvQ3O5w1ysuYAHA" width="400" alt="www.youtube.comで接続が拒否解決">