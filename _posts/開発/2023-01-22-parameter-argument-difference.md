---
layout: post
title: "parameterとargumentの違い"
slug: parameter-argument-difference
comments: false
tags: [developer]
---
# parameterとargumentの違い
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="parameterとargumentの違い"  width="300" >
業務でプログラミングを使用する場合は開発用語について理解して使わなければなりません。  
開発者ってプログラミングができるということよりもコミュニケーションの用語が大事です。  
なので、今回はパラメーターとアーギュメントの違いについて簡単に説明をします。  
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
  
## parameterとは
プログラミング上のparameter(パラメーター)は制限した関数の中にある仮引数を意味します。  
```javascript
function Sum(a, b) {
  return a + b;
}
```
上記のソースコードで関数の隣にあるa, bがパラメーターになります。  

## プログラミングのargumentとは
プログラミング上のargument(アーギュメント)は外部の関数を使用する時に、  
関数の括弧の中にある実引数を意味します。  
```javascript
...

Sum(17, 30);

...
```
17, 30が引数でも読めますが、正しい表現は実際の値を持っているので実引数になります。  

## 最後に
開発者って海外の人と仕事をする場合もありますし、  
何よりも情報を検索する時に英語名の開発用語を勉強しておくと、  
簡単に欲しい情報を得ることが可能です。  
実際に仕事をする時に日本語の開発用語を使ってもいいですが、  
プログラミングのモトは英語からきたものなので英語の用語もしっかりと勉強していきましょう。  