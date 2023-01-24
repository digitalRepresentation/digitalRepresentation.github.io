---
layout: post
title: "[typescript]Genericの解説"
slug: typescript-generic
comments: false
tags: [developer]
---
# typescriptのジェネリック(generic)
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="typescript  generic"  width="500" >


## genericとは
ジェネリック(generic)はC#, Java等の言語で再利用性が高いコンポーネントを作る時に活用なるのが特徴です。  
一つの型より複数の型で動作するコンポーネントを生成する時に使われます。  
ジェネリック(generic)を使用するのはUnion Typeと同じ感じでパラメータやreturn値等一つの型ではない場合にtypescriptでは`any`を使うのが一般的ですが、  
ジェネリック(generic)を使う時はUnion Typeと同じく再利用性に良いです。  

文字や数字、Booleanの値を出力する関数はジェネリック(generic)をどうやって使うのか見てみましょう。  
```typescript
function unionTypeFunc(parameter: string | number) {
  function printText(x: any): any {
    return x;
  } 

  function printText<T>(x: T): T {
    return x;
  }

  printText('hello'); // 'hello'
  printText(30); // 30
  printText(false); // false
}
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
  
`any`型でした場合は`type checker`をしないので今後runtime errorになる問題が高いです。  
しかし、ジェネリック(generic)を利用すれば`type checker`だけではなくアーギュメントに合わせてreturn値も設定が可能です。  
※ジェネリックの`T`は`Type`を意味します。二つのジェネリックを書く場合は`T`と`U`を使うのが一般的です。  

## Generic Type
functionを利用してGenericのinterfaceを作るのが可能です。  
#1と#2のような形で実装するのが可能です。  
関数で定義した際はJavascriptの関数宣言と一緒で変数にした場合は関数式と同じです。  
```typescript
// 関数宣言
function printText<T>(text: T): T {
  return text;
}

// #1 関数式
let str: <T>(text: T) => T = printText;
// #2 関数式
let str: {<T>(text: T): T} = printText;
```

[Generic Typeの参考サイト](https://stackoverflow.com/questions/48967142/typescript-what-are-call-signature-of-an-object-literal-and-how-can-they-be-use)