---
layout: post
title: "[typescript]watchモード"
slug: typescript-watch-mode
comments: false
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1GDoTF_NzXa5Vfgc-63SX7EoVypdn3Rov"  width="700" alt="typescript">

## 一つのtypescriptファイルを自動でコンパイルする方法
typescriptを変更するたびに変更内容をページで自動に反映されたい時はwatchモードを使えば問題ないです。  
watchモードを使うとtypescriptがファイルを観察してファイルに変更内容があるたびにまたコンパイルすることになります。  
使い方は下記の通りです。watchかwをつければいけます。  
```typescript
tsc app.ts --watch
tsc app.ts --w
```
デメリットは一つのファイルで使うときだけなので、具体的にファイル名を指定しないといけないです。  
いまは一つのファイルでやっていますが、規模が多いプロジェクトは使いません。  

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
  
## typescriptファイルが複数の場合どうやって自動でコンパイルするのか。
複数以上のファイルの変更内容がある場合はファイルごとにコンパイルするので手間がかかります。  
watchモードに入ってtscを入力するやり方にすると小パイルが簡単にいけますでしょう。  
ファイルを指定しなくてもwatchモードで全てのプロジェクトフォルダを確認するし、  
変更内容が反映されている全てのtypescriptファイルをもう一度コンパイルするのが可能です。  
下記のコマンドを入力します。  
```typescript
tsc --init
```
特定のファイルを入力せずにただtsc --initを実行するだけです。  
このコマンドはプロジェクトをtypescriptプロジェクトだと最初に一回だけ実行すれば大丈夫です。  
つまり、このコマンドが実行されるフォルダの全ての項目を教える役割をします。  
なので、<span style="color:red">正しいプロジェクトルートにコマンドを入力するのが大事です。</span>
実行すればtsconfig.jsonファイルが出ます。  

## watchモードコンパイル方法
tscというコマンドを入力すると全てのtsファイルがコンパイルできます。  
なので、時間はかかる場合があります。  
```shell
tsc
```
その後でwatchモードに結合します。  
```typescript
tsc --watch
tsc --w
```