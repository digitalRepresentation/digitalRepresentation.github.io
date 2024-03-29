---
layout: post
title: "[os]processとthreadの違い"
slug: os-process-vs-thread
comments: false
tags: [developer]
---
# [os]processとthreadの違い
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="プロセスとスレッドの違い"  width="500" >
プロセスとスレッドは独立的なものです。  

## プロセスとは
プロセスは実行中のプログラムのインスタンスです。  
インスタスが生成すると言う意味はプログラムの実行に必要な内容がPCのメモリ（RAM）に積載されると言う意味です。  
プロセスとプログラムは同じだと言う話は正しくありません。  
プログラムはどう言う作業をするために実行できるファイルを意味して、  
プロセスはメモリに積載されてCPUのresourceを割り当ててプログラムが実行されている状態です。  
プロセスは一回に複数の作業を遂行するために他のプロセスを生成することが可能です。  
作られたプロセスを子供プロセス、メインプロセスを親プロセスと言います。  
各々のプロセスは独立されたメモリにあって、お互いに共有できません。  

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
  
## プロセスの仕組み
<img src="https://drive.google.com/uc?export=view&id=1wEPsdM5eyN8zOJr5JzefQHSU67UGPM3c" alt="プロセスの仕組み"  width="700" >

stack area: 呼び出された関数が終了すると戻される住所をstackに保存したり、変数使用範囲に影響を与えるエリアを実装する時に使用します。  
heap area: 動的に割り当てるデータのために存在するエリアです。  
data area: コードが実行しながら使用した変数やファイルのいろんなデータが集まっています。  
text area: プログラマが作成したプログラムがあるエリアです。  
※Text, Dataエリアは宣言する時に大きさが決められる定的なエリアで、stackとheapはプロセスが実行される間に動的に変わるエリアです。  

## スレッドとは
スレッドは一つのプロセスの中で動作される色々実行の流れみたいなものです。  
プロセスは一つ以上のスレッドをもっつのが可能です。  
同じプロセスの中にある全てのスレッドは同じHeap areaを共有します。  
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
  
## プロセスとスレッドの違い
1. プロセスは独立的で他のプロセスに含まれていない反面、全てのスレッドはプロセスの内に共有ができます。  
2. プロセスはメモリおよび他のresourceを含まれるので個別的に存在できますが、スレッドは個別的に存在できません。  
3. プロセスはプロセスの間に通信を利用してお互いに通信ができます。しかし、スレッドは同一な住所エリアを共有できるので、お互いに直接通信ができます。  
4. プロセスはresourceが共有できないですが、スレッドはresourceを共有する。  