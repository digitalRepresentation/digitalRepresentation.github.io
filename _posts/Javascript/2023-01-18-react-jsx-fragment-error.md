---
layout: post
title: "JSX フラグメントには対応する終了タグがありません。エラー解決方法"
slug: react-jsx-fragment-error
comments: false
tags: [javascript, developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="JSX フラグメントには対応する終了タグがありません。エラー解決" width="700">

## JSX フラグメントには対応する終了タグがありません。エラー
JSXを使う時に上記のエラーを出会ったことありますでしょうか。  

```javascript
  return (
    <div class="title">水曜日夜は勉強する時間となります。
      <p>おいしいものも食べながら勉強しましょう。
    </div>
  );
```

私が記載した内容にも同じエラーになります。  
解決はどうやってできますでしょうか。  
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
  
## JSX フラグメントには対応する終了タグがありません。エラー解決方法
私の場合はpタグの閉じタグがありませんでした。  
JSX上に締めタグがない場合はエラーになりますので、  
下記の方法みたいに解決するのが可能です。  
```javascript
  return (
    <div class="title">水曜日夜は勉強する時間となります。
      <p>おいしいものも食べながら勉強しましょう。</p>
    </div>
  );
```