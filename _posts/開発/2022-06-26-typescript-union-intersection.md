---
layout: post
title: "[typescript]Union typeとintersection typeの解説"
slug: typescript-union-intersection
comments: false
tags: [developer]
---
# TypescriptのUnion typeとintersection typeの解説
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="typescript union type intersection type"  width="500" >


## Union Typeとは
ユニオンタイプ(Union Type)とはJavascriptのOR演算子`||`と同じく`AまたはB`と同じ意味です。  
```typescript
function unionTypeFunc(parameter: string | number) {
  // ...
}
```
parameterにあるdata typeはstringやnumberのみ許可します。  
このように`|`演算子を利用して複数のタイプを連携する方式をUnion Typeをと言います。  

## Union Type(literal type)
一般的なdata type以外も文字列を使用してunion typeを使えます。  
下記のように小さな単位のタイプの集まりをユニットタイプ（Unit Type）とも呼ばれるりーたらリテラル型です。  
```typescript
 function unionTypeFunc(parameter: "asia" | "europe" ) {
  // ...
}
unionTypeFunc("asia"); // OK
unionTypeFunc("afreeca"); // Error
```

## Union Typeのメリット
特定の関数に二つ以上のパラメータの値が必要な場合にtypescriptがよくわからない人は`any`を使用しますが、  
Union Typeを利用すると二つ以上のタイプを持っていくのが可能なので、typescriptの`Type Checker`機能が使えます。  
data typeを`any`にする場合は`Type Checker`が無効になるのでruntime errorにつながる恐れがあります。  

## インターセクション型(intersection type)
インターセクション型（intersection type）は全ての型を満足する一つの型を意味します。  
`&`演算子はAND演算子みたいな感じでTruckとRobotのプロパティを持っているfutreTruckを使う際に全てのプロパティを全部作成し冪です。  
```typescript
interface Truck {
  name: string;
  speed: number;
}

interface Robot {
  name: string;
  transformation: string;
}

type futureTruck = Truck & Robot;

let JapanFutreTruck: futureTruck = {
    name: "ichi",
	speed:  141,
    transformation: "test"
};
```

## Union typeを使う時に注意するべきな点
Union typeとintersection typeについての説明をしました。  
論理的にUnion TypeはOR、intersection typeはANDだと考える人が多いですが、interfaceと同じtypeを扱う時は  
このような論理的な思考を注意すべきです。  

```typescript
interface Truck {
  name: string;
  speed: number;
}

interface Robot {
  name: string;
  transformation: string;
}

function JapanFutreTruck (parameter: Truck | Robot) {
  parameter.name; // OK
  parameter.speed; // Error type error
  parameter.transformation; // Error type error
};
```
typescriptの観点では`JapanFutreTruck()`を使う時にアーギュメントの型がTruckかRobotどちらが来るのかわからないので、  
どの型が入ってもエラーにならない方向で型推論するようになります。  