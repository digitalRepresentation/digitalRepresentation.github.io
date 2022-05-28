---
layout: post
title: "atagの_blankセキュリティと、性能問題について"
slug: atag-noopener-noreferrer
comments: true
tags: [developer]
---
atagの_blankセキュリティと、性能問題について

## aタグで_blankをする時に性能とセキュリティが良くないことを知っていますか。
aタグで_blankを使用する時は性能が良くない場合もあります。  
A.htmlからB.htmlに移動する時にB.htmlにjavascriptが多い場合に  
A.htmlに性能が悪くなることがあります。  

## aタグの_blankは誰でもwindows.openerを触ることが可能です。
windows.openerはリダイレクトされる機能です。　　
Tabnabbing attackされることがあります。  
簡単にいうとハッカーがfishingサイトを作ってそこに入ったら、  
windows.openerが変わってしまって、本当のサイトにatagのwindow.openerが変わるので、  
本当のサイトからfishingサイトに連携される不思議な状態となります。  

## Tabnabbing attackをどうやって防ぐのか。
二つの解決方法があります。  
rel属性にnoopener, noreferrerをどちらをつけたら問題解決です。

## noopenerのメリットは？
noopenerはwindows.openerが使えなくなります。  
それでTabnabbing attackを防ぐのが可能です。  
SEOとしても問題ないです。  
性能も良くなります。移転先と移転前のサイトのプロセスが切れるので、  
移転先のjsが多くても本サイトの速度は遅くなりません。  
IEは対応してないので、6月15日ごろにIEが終了するので使えれば良いと思います。  
Chrome, Safari, Firefoxなどは自動でnoopenerがつけるので大丈夫です。  

## noreferrerのメリットは？
noreferrerはヘッダーのrefer情報をなくします。  
性能の面はnoopenerと同じなので使っても良いです。  
SEOはA.htmlサイトからB.htmlに転移する時にB.htmlがどこから移動したのかデータが残ってないです。  
なので関連ないサイトは良いけど、関連ある場合はGAで情報取得ができなくなります。  
しかしIEも対応するので良いかと思います。  
IEは6月にサービス終了してもEdgeのIEモードがあるので2029年までサービス提供するようです。  
