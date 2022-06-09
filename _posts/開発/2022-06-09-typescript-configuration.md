---
layout: post
title: "typescript環境構築をする方法"
slug: typescript-環境構築をする-方法
comments: true
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="typescriptの環境構築"  width="700" height="370">

# typescriptの環境構築する手順
typescriptの環境構築の手順をご説明いたします。  
簡単に説明すると下記の内容をすれば問題ないですが、細かく画像でご説明いたします。  
1. npmを使うためにnode.jsをinstallします。  
2. typescriptホームページでnpmを使用してtypescriptを設置します。  
3. プロジェクトのルートからnpm initを叩きます。基本的にenterキーを押すと、defaultなので構いません。  
4. 内部にpackage.jsonファイルが入れることを確認します。  
5. npm install --save-dev lite-serverを通してこのプロジェクトに使われるツールを設置するために叩きます。  
6. package.jsonファイルに入ってlite-serverを記載します。  
7. npm startを叩きます。  
8. tsc --initを入力するとtsconfig.jsonファイルができます。  

## npmを使用するため、node.jsをinstallします。
typescriptを使うためにはnpmが必要です。  
node.jsをダウンロードするとnpmが入っているので、node.jsをダウンロードしてください。  
[nodejsページ](https://nodejs.org/ja/).  
二つのバージョンがありますが、最近のバージョンは安定的ではないので、  
推奨版を使用してください。  
<img src="https://drive.google.com/uc?export=view&id=1TLk2cjUsgISYSXrHp6TEfox3wlysHFmI" width="800" height="300" alt="nodejs設置方法">
設置が完了できましたら、commandでnodeバージョンが確認できます。  
```shell
node --version
```

## typescriptホームページでnpmを使用してtypescriptを設置します。
typescriptを設置してください。  
[typescriptページ](https://www.typescriptlang.org/download).  
npmがあるのでinstallをしてください。  
```shell
npm install typescript --save-dev
```
設置が完了できましたら、バージョンを確認してください。  
```shell
tsc --version
```
tsc versionが確認できない場合があります。  
用語 'tsc' は、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。のメッセージが出た場合はエラー解決方法を記載しましたので、ご確認ください。  
[tscエラー解決](https://digitalrepresentation.github.io/2022/06/03/typescript-tsc-error/).  

## プロジェクトのルートからnpm initを叩きます。
基本的にenterキーを押すと、defaultなので構いません。  
全部最後までenterキーを押してください。  
<img src="https://drive.google.com/uc?export=view&id=1NxZgpXYa1HWYJDkkcflTCmCbRcraQeSq" width="800" height="600" alt="npm init入力方法">

## 内部にpackage.jsonファイルが入れることを確認します。  
package.jsonはサーバーに関する内容なので、  
ファイルがルート内にあレバ問題ないです。  
<img src="https://drive.google.com/uc?export=view&id=1BumTdbH-bNLZTUN_YYZckfDtqSZryUWT" width="200" height="200" alt="package json">

## npm install --save-dev lite-serverを通してこのプロジェクトに使われるツールを設置するために叩きます。  
lite-serverを通してこのプロジェクトに使われるツールを設置できるように叩きます。  
これは開発中に助かるツールでメインコードの一部に実行されるコートは含まれていません。  
```shell
npm install --save-dev lite-server
```
<img src="https://drive.google.com/uc?export=view&id=124Nou7OPrxMwfJLbFAF2lbmEiWFdl6WA" width="1000" height="200" alt="lite-server">

## package.jsonファイルに入ってlite-serverを記載します。  
色んなファイルができましたが、package.jsonに入って内容を修正します。  
<img src="https://drive.google.com/uc?export=view&id=1iw1mHWvMHv5KQRa9OvdtuynkB3n6RmE-" width="1600" height="700" alt="lite-server">
```javascript
"test": "echo \"Error: no test specified\" && exit 1",
"start": "lite-server"
```

## npm startを叩きます。
npm startを叩いてサーバーをonします。  
localhost:3000のアドレスでサーバーが入れます。  
```shell
npm start
```
<img src="https://drive.google.com/uc?export=view&id=1kK45RqnuJCQIgfo3NLni9jF_Tn5A1fag" width="700" height="400" alt="lite-server">

## tsc --initを入力するとtsconfig.jsonファイルができます。  
プロジェクト全部watchモードを使うのであれば、下記の内容を叩いて使います。  
watchモードについては説明文を記載しましたので、ご確認ください。  
[typescriptWatchモード](https://digitalrepresentation.github.io/2022/06/04/typescript-watch-mode/).  
```shell
tsc --init
```

<img src="https://drive.google.com/uc?export=view&id=1kK45RqnuJCQIgfo3NLni9jF_Tn5A1fag" width="700" height="300" alt="lite-server">



ここまですると、typescriptをプロジェクトで管理する設定が完了します。  