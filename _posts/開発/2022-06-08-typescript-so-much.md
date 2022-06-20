---
layout: post
title: "typescriptとは"
slug: typescript-so-much
comments: true
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="typescriptとは" width="700">

# typescriptとは
typescriptはjavascriptの<span style="color=red;">SuperSetです。  
つまり、typescriptは結局javascriptを元に作った言語です。  
typescriptは新しく作った言語ではなく、javascriptの言語を使用し、新しい機能とメリットを追加する言語で、  
javascriptコードをより簡単に強く作成できるように提供されています。  

## typescriptのメリット
typescriptのコンパイラーはエンジニアにより簡潔な構文と作業をより簡単にできるようにする解決方法を提供します。  
typescriptを使えば複雑なjavascriptをよりかっこいいコードにコンパイルできるようにします。  
javascriptのtypeを追加し、javascriptの追加機能に機能を追加します。  
この機能はscriptが実行してブラウザでruntimeエラーが発生する前にコードのエラーを開発者として事前に確認できるメリットがあります。  
つまり、新しい機能でより良いコードを提供するだけではなく、開発中にruntimeエラーを発生するエラーを初期開発するときに見つけて修正できるようにエラー検査を提供します。  
typescript設定ファイルのjsonでoptionを追加するだけでより強くコンパイルすることが可能です。　　

## typescriptのデメリット
typescriptはブラウザと同じくjavascript環境で実行できません。  
ブラウザはtypescriptを実行するのができません。  
node.jsもtypescriptが実行できません。  
javascriptが実行できる環境ではtypescriptがサポートしません。  

## typescriptはプログラミング言語、ツールです。
コードを実行してtypescriptコードをjavascriptでコンパイルする強いコンパイラーです。  
コードとtypescriptを作成して結果的に得られるものはjavascriptですが、  
javascriptコードを作成するのではなく、新しい機能とメリットを全て備えているtypescriptコードを得られます。  
新しい機能をjavascript解決策でコンパイルするのがtypescriptのコンパイルです。  

## typescriptを使う理由
プログラマが予想してないエラーが発生するからです。  
下記の内容をみるとプラスする関数があります。  
数字をプラスしようと思いましたが、  
stringの値が入ってしまって、数字のプラスではなく、文字の結合になります。   
これはjavascriptで見つけるエラーで技術的なエラーではないです。  
javascriptはプログラマに優しく動作ができているので、  
こういうミスを経るためには必ずtypescriptを使えばコンパイルする際にエラーを見つけるので、防ぐのが可能です。  
```javascript
function calculator(a, b) {
    return a + b;
}

console.log(calculator('2', '3'));
```