---
layout: post
title: "値を比較する時にundefinedとnullどちらが良いのか"
slug: javascript-undefined-null-comparison
comments: true
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL"  width="700">
値を比較する時にundefinedとnullどちらが良いのか    

## undefined、nullとは
javascriptのundefinedは値が未定義する時のデータタイプです。  
javascriptのnullは値がないという値でデータタイプはObjectです。  
値がないというのは空白ではなくて値がnullという意味です。  
※nullのタイプがobjectというのはjavascriptのバグだと出ていますが、javascriptの仕様だと思えば問題ないです。　 

## undefinedとnullの違い
変数の宣言した場合にundefinedとなってしまいます。  
nullはプルグラマが明示的に指定した場合にnullとなります。  

```javascript
let variable;
console.log(variable) // undefined
variable = null;
console.log(variable) // null
```


## javascriptでデータの存在有無チェックする方法
データの存在有無を確認するときは基本タイプ(string, number, boolean)と参照タイプのObjectが違います。  
基本タイプはnullで値をチェックする方が一般的です。　 
未定義の変数を比較するのはよろしくないです。  
```javascript
// 必ず変数は値を入れておくことが大事。
let variable = null;
let area_flag = false;
if(area_flag === true) {
    variable = true;
}
if(variable !== null) {
    //処理
}
```

Objectタイプの場合はLibによりますが、
値の存在有無を確認する際はundefinedが一般的です。  
たまにnullで比較もできますが、  
それはメソッドのreturnが何もない時にnullをreturnするので、そういう場合はnullで存在有無をチェックしましょう。  
```javascript
const array = [1, 2, 3];
if(array[3] !== undefined) {
    //処理
}
```

### まとめ
比較するときはもっと厳しい===を使って比較をします。  
値の存在チェックをする際はprimary typeはnullでreference typeはundefinedを比較する習慣を作っていきましょう！  