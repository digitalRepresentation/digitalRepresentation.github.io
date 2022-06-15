---
layout: post
title: "「www.youtube.comで接続が拒否されました。」のエラー対策"
slug: youtube-iframe-error
comments: true
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1atPJmnA7V6dolOLwA5DLUZQx8To5y08B" alt="typescriptとは"  width="500" alt="www.youtube.comで接続が拒否されました。">

# 「www.youtube.com で接続が拒否されました。」のエラー対策
youtubeの動画をiframeのsrcで挿入する際に、www.youtube.comで接続が拒否されました。というエラーが出ました。 
エラーはurlの描き間違えです。  
このままurlを入れるとiframeで読み込まれないです。  

<img src="https://drive.google.com/uc?export=view&id=1trmBl-Do9JLcqCq1c6OrsJaMW78gbJtO" alt="typescriptとは"  width="700" alt="www.youtube.comで接続が拒否">

なので下記のurlみたいにshortsをembedに変更すれば問題解決となります。  
修正前：www.youtube.com/<span style="color:red; font-weight: bold;">shorts</span>/c3UIJLv-bzs  
修正後：www.youtube.com/<span style="color:red; font-weight: bold;">embed</span>/c3UIJLv-bzs  

## 「www.youtube.com で接続が拒否されました。」解決
下記のようにshortsをembedに修正すると、  
動画が表示されます。  

<img src="https://drive.google.com/uc?export=view&id=1UDyBVNWaxcFJpPmSNUvQ3O5w1ysuYAHA" alt="typescriptとは"  width="400" alt="www.youtube.comで接続が拒否解決">