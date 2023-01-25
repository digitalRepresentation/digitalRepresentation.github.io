---
layout: post
title: "Missing script: 'start'のエラー解決"
slug: npm-not-found-error
comments: false
tags: [javascript, developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Missing script: 'start'のエラー解決" width="700">

# Missing script: 'start'のエラー解決
```terminal
npm ERR! Missing script: "start"
npm ERR! 
npm ERR! Did you mean one of these?
npm ERR!     npm star # Mark your favorite packages
npm ERR!     npm stars # View packages marked as favorites
npm ERR! 
npm ERR! To see a list of scripts, run:
npm ERR!   npm run

npm ERR! A complete log of this run can be found in:
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
  
Reactのプロジェクトを実行すると、reactがないというエラーが発生しました。  
こちらのエラーが発生する理由はターミナルの場所が正しくないからです。  
ですので、プロジェクトがある場所に移動してnpm startコマンドを叩いたら解決できます。  

```terminal
$ cd project-name
$ npm start
```

上記の方法だと解決できます。  
しかし、うまく行ってなかった場合はReactを再設置しましょう。  
そして、npmよりyarnが速度が速いため、yarnを使いましょう。  

[React設置手順書](https://digitalrepresentation.github.io/2023/01/16/react-configuration/)  
このリンクはwindows, mac向けでyarnとnpmどっちもできるように手順書が書かれています。  
reactを再設置したい時はぜひご覧くださいませ。  