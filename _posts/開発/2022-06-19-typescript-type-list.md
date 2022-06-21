---
layout: post
title: "typescriptのtypeとは"
slug: typescript-typeとは
comments: true
tags: [developer]
---
# typescriptのtypeとは
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="タイプスクリプトのタイプ"  width="700" >
typescriptの型は12個あります。  
typeを名義する際は必ず小文字で入力します。
1. String  
2. Number  
3. Boolean  
4. Object  
5. Array  
6. Tuple  
7. Enum  
8. Any
9. Void
10. Null
11. Undefined
12. Never

## typescriptのタイプ「String型」
typescriptのstring型の書き方です。
```typescript
const strVariable: string = "hello";
```
:を利用してjavascriptのコードにtypeを定義する方式をオブジェクトの型注釈(Type Annotation)と言います。  

## typescriptのタイプ「Number型」
typescriptのnumber型の書き方です。  
```typescript
const numVariable: number = 10;
```

## typescriptのタイプ「Boolean型」
typescriptのboolean型の書き方です。  
```typescript
const isVariable: boolean = false;
```

## typescriptのタイプ「Object型」
typescriptのobject型の書き方です。  
```typescript
const apple: object = {
	price: number = 200,
  name: string = "Seoul Apple"
}
```

## typescriptのタイプ「Array型」
typescriptのarray型の書き方です。  
```typescript
const arrCount: number[] = [1, 2, 3];
const arrCount2: Array<number> = [1, 2, 3];
```

## typescriptのタイプ「Tuple型」
配列の長さが固定で、各々の要素のタイプが指定されている配列形式です。  

typescriptのtuple型の書き方です。  
```typescript
const arrEmployee = [string, number] = ["Watanabe", 3];
```
上記のtupleは必ず二つの要素を持つべきです。  
一番目の要素はstringで、二番目の要素はnumberではないとエラーになります。  
定義してないタイプまたはindexで接近する場合はエラーになります。  
```typescript
arrEmployee[1].concat('!'); // Error, 'number' does not have 'concat'
arrEmployee[5] = "Hello;" // Error, Property '5' does not exist on type '[string, number]'
```

tupleのタイプはpushは例外的にtupeで許可されるので、タイプスクリプトでこう言うエラーを見つけないですが、少なくとも正しくない値を入れません。  
```typescript
const person = {
	role: [number, string];
} = {
	role: [2, 'author']
}

person.role.push('admin'); // errorですが、typescriptはコンパイラする
person.role[1] = 10; //error 

person.role = [3, 'hidden']; // ok
person.role = [0, 'admin', 'user']; // error
```

## typescriptのタイプ「Enum型」
Enumは定数の集まりです。javascriptではない機能です。  
typescriptのenum型の書き方です。  
```typescript
enum Auth { Guest, Leader, Admin }
const kim: Auth = Auth.Admin; // 2
```

Enumはindexでも読み込まれます。  
```typescript
enum Role { ADMIN = 5, READ_ONLY, AUTHOR };

Role.ADMIN; // 5
Role.READ_ONLY; // 6
Role.AUTHOR // 7
```

Enumのindexを変更して使用するのが可能です。  
indexを0から始めたくない場合は宣言するときに数字を入れて制御が可能です。  
if検査に活用したり、タイプ割り当て(Type Assignment)に活用しても良いです。  
visual studio codeを使用すれば自動完成機能があるのでミスをなくすことができて、生産性が上がります。  
```typescript
enum Role { ADMIN = 5, READ_ONLY, AUTHOR };

Role.ADMIN; // 5
Role.READ_ONLY; // 6
Role.AUTHOR // 7
```

## typescriptのタイプ「Any型」
単語のそのものの意味で、全てのタイプについて許可します。  
```typescript
const str: any = 'hello!';
const num: any = 23;
const arr: any = ['a', 2, true];
```

### typescript Anyタイプのデメリット
anyは全てのタイプを許可するので良いタイプだと思いますが、大きいデメリットのせいで、  
なるべくanyを使わない方が良いです。  
anyタイプを使用する全ての部分はタイプスクリプトのコンパイラーが動作しなくなります。  
any属性、any変数がどんなタイプも保存しないのでコンパイラーが検査する部分がなくなります。  
なので、どんな値や種類のデータがどこに保存されるのか全然わからない場合、runtime検査をする場合等、作業の範囲を狭くするためにanyをつけば良いです。  
他の場合はanyを使わない方が良いです。  
作業するときに使うタイプをばっちりとまとめて欲しいです。  

## typescriptのタイプ「Void型」
変数はundefined, nullだけ割り当てて、関数は返却する値を設定できないタイプです。  
「void」を使えずにinterface engineに任せるのも良いです。  
typescriptのvoid型の書き方です。
```typescript
count unuseful: void = undefined;
function notuse(): void {
	console.log('sth');
}
```

## typescriptのタイプ「Never型」
関数の終わりに到達しないと言う意味を持っているタイプです。  
typescriptのNever型の書き方です。
```typescript
function neverEnd(): never {
	while (true) {

	}
}
```