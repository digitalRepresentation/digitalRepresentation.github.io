---
layout: post
title: "typescriptの「型 'string[]' を型 '[string, string]' に割り当てることはできません。」エラー"
slug: typescript-tuple-type-error
comments: false
tags: [developer]
---
# typescriptの「型 'string[]' を型 '[string, string]' に割り当てることはできません。」エラー
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="型 'string[]' を型 '[string, string]' に割り当てることはできません。ターゲットには 2 個の要素が必要ですが、ソースに指定する数はそれより少なくても構いません。"  width="500" >

typescriptの変数に先にtypeを設定して、それをtupleにするとエラーになる場合があります。  
  
型 'string[]' を型 '[string, string]' に割り当てることはできません。  
ターゲットには 2 個の要素が必要ですが、ソースに指定する数はそれより少なくても構いません。  
  
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-7886659064712565"
     crossorigin="anonymous"></script>
<!-- 광고2 -->
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7886659064712565"
     data-ad-slot="1101493367"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>

    
## typescriptの「型 'string[]' を型 '[string, string]' に割り当てることはできません。」エラー発生理由
stringListに二つのstringがあると仮定します。  
その値をtupleに入れようとするとエラーになります。  
```typescript
const stringList = ["jin", "young"];
const tuple: [string, string] = stringList;
```
string[]は[string, string]の部分集合じゃないからです。  
反対なら可能です。  

## typescriptの「型 'string[]' を型 '[string, string]' に割り当てることはできません。」エラー解決方法
1. stringListとtuple変数のtypeを同じく設定します。  
```typescript
const stringList: [string, string] = ["jin", "young"];
const tuple: [string, string] = stringList;
```

2. stringListをtypeを[string, string]に指定して、tupleのtypeをstring[]にします。  
```typescript
const stringList: [string, string] = ["jin", "young"];
const tuple: string[] = stringList;
```
    
typescriptはtypeの設定が厳しです。  
なので、typeを設定しない時にはどういうtypeになるのか、ちゃんと認識して使いましょう。  
それが難しい場合は事前にtypeを設定して使えばいいです。  
