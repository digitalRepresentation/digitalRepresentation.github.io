---
layout: post
title: "[typescript]classの使い方とアクセスアクセス修飾子(public/private/protected)について解説"
slug: typescript-class-使い方-アクセスアクセス修飾子-public-private-protected-について解説
comments: true
tags: [developer]
---
# Union typeとintersection type
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov" alt="typescript class"  width="500" >


## Classとは
typescriptは ES6から導入された`class`キーワードを完璧にサポートします。  
new演算子を利用してinstanceして使われます。  

## readonly
readonlyを使用すれば`name`を読み込み専用に作りますので修正・削除するのが不可能です。  
```typescript
class People {
	readonly name: string;
  age: number;
	constructor(readonly n: string, age: number) {
		this.name = n;
    this.age = age;
  }
}

let kobayashi = new People('kobayashi', 30);
kobayashi.age = 20; // ok
kobayashi.name = 'jinyoung'; // error
```

## アクセス修飾子(public/private/protected)
typescriptでは**アクセス修飾子があります。**  
public: 外部から使われる変数です。  
private: 自分のClass内のみアクセス可能
protected: **継承されたクラス内**でアクセス可能（継承`extends`を使います。）
下記のようにmember variableを書かなくてもconstructorに書くとmember variableとして使われます。
```typescript
class People {
//	name: string;
//  age: number;
	constructor(protected name: string,public age: number) {}
}

class SoccerPeople extends People {
  constructor(name: string, age: number, private speed: number) {
		super(name, age);
	}
}

let kobayashi = new SoccerPeople('kobayashi', 30, 15);
kobayashi.age = 20; // ok
kobayashi.name = 'jinyoung'; // error
kobayashi.speed = 20; // error
```
