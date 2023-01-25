---
layout: post
title: "Reactのコンポーネント中にdomのidを使わない理由"
slug: react-dom-why-do-i-need-id
comments: false
tags: [javascript, developer]
---
# Reactのコンポーネント中にdomのidを使わない理由
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Reactのコンポーネント中にdomのidを使わない理由" width="600">
Reactのコンポーネントもidを使うことができます。  
しかし、コンポーネントにidをつけると、そのままレンダリングするからです。  
呼び出すファイルで同じコンポーネントを呼び出す場合に、  
同じidが振替して呼ばれるので、よくないソースコードになります。  
  
  
  
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
    
HTMLのidはユニークな存在なので、必ず1個持つしかないです。  
大体idを使わずにclassで欲しい機能を実装することが可能ですが、  
他のライブラリとフレームワークを使うと息はidを使うべき状況もあります。  
この時はidの後ろにばん後をつけて重複idができないようにするのがベストです。  
例えば、div1, div2, div3みたいな感じで重複idにならないようにするのが大事です。  
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
  
  
## reactはid使う時にどうすれば良いのか
reactはref、hookを使えば解決できます。  
refはReact.createRef()で生成が可能で、ref attributeを通してreactエリメンとに貼り付けて使えます。  
公式のページがありますので、ご参考にしてください。  
  
[https://ko.reactjs.org/docs/refs-and-the-dom.html](https://ko.reactjs.org/docs/refs-and-the-dom.html)  