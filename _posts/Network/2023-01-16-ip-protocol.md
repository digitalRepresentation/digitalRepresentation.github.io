---
layout: post
title: "インターネットプロトコルとは【わかりやすく説明】"
slug: internet-protocol-ip
comments: false
tags: [network]
---
<img src="https://drive.google.com/uc?export=view&id=1yUekx5KlNiJ8pZqV6peX_dFFnHc_ZOva"  width="700" alt="">
  
## インターネットプロトコルとは【わかりやすく説明】
Internet ProtocolのProtocolは「データ通信」という言葉ですが、「外交」にも翻訳できます。  
つまり、インターネット上でお互いに約束した規則をもとに「外交」をする行為を言います。  
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
  
### インターネットプロトコルの役割
指定したIP住所(IP Address)にデータを送ります。  
パケット(Packet)という通信単位にてデータを送ります。  

## メッセージをただ送るのではなく、IP Packetの規則の通りに送ります。  

クライアントパケット  
出発 1.1.1.1  
到着（目的） 2.2.2.2  
内容　Hello World  
    
↓ (ノードを通して送ります。)  
  
サーバパケット  
出発 2.2.2.2  
到着（目的） 1.1.1.1  
OK  
  
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
  
## インターネットプロトコルの限界
### コネクションレス
パケットをもらう対象がないまたはサービスができない状態でもパケットを送ります。　 

### 非信頼
→ パケットを送る途中にサーバがオフになったら、何も表示しないので問題になります。  

### パケット送る順序問題発生
パケットが容量が大きい場合と、大きくない場合は送った順序に関係なく、パケットを送るので問題になります。  

### プログラム区分
同じIPを使用するサーバで通信するアプリケーションが二つ以上ならどのプログラムを使えば良いのかわからなくなる。