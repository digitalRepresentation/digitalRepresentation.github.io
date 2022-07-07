---
layout: post
title: "javascriptのsortを使う時に数字がうまく昇順と高順にならない場合の対策を紹介します。"
slug: javascript-array-sort
comments: false
tags: [developer]
---
# javascriptのsortを使う時に数字がうまく昇順と高順にならない場合の対策を紹介します。
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="javascriptのsort数字やり方" width="700">
javascriptのsortメソッドは配列の要素を整列します。原本の配列を直で変更します。
sortメソッドは基本的には昇順に要素を整列します。  
sortの反対メソッドはreverse()です。
```javascript
const colors = ['pink', 'red', 'blue', 'black'];
// 基本的には昇順に整列する。
colors.sort();
```

## 数字の場合にjavascriptのsortを使う時に意図した通りにいかないのは？
文字列の要素の配列のsortは問題ありません。しかし数字飲みになっている要素で配列を整列する時は注意するべきです。  
```javascript
const testScores = [30, 20, 10, 40, 1, 5, 6];
// 基本的には昇順に整列する。
testScores.sort();
// [1, 10, 20, 30, 40, 5, 6]
console.log(testScores);
```
sortメソッドの整列順序はユニコードコードポイントの順序を従います。配列の要素が数字のタイプでも配列の要素を一時的に文字列に変換した後にユニコードのコードポイントの順序が基準になります。  

## javascriptの配列の数字型のsortはどうすれば良いか。
数字の要素を整列する時はsortメソッドに整列順序を定義する比較関数を引数で伝達すべきです。

```javascript
const testScores = [30, 20, 10, 40, 1, 5, 6];
// 数字の昇順に整列する。比較関数のreturn値が0より小さくとaを優先して整列する。
testScores.sort((a, b) => a - b);
// [1, 5, 6, 10, 20, 30, 40]
console.log(testScores);
// 数字の降順に整列する。比較関数のreturn値が0より小さくとbを優先して整列する。
testScores.sort((a, b) => b - a);
// [40, 30, 20, 10, 6, 5, 1]
console.log(testScores);
```

javascriptのsortメソッドの使い方について解説しました。javascriptのArrayは活用できるメソッドが多いので次回も紹介していきたいと思います。