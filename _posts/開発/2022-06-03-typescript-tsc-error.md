---
layout: post
title: "用語 'tsc' は、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。"
slug: typescript-tsc-error
comments: true
tags: [developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL"  width="700" height="370">

用語 'tsc' は、コマンドレット、関数、スクリプト ファイル、または操作可能なプログラムの名前として認識されません。名前が正し  
く記述されていることを確認し、パスが含まれている場合はそのパスが正しいことを確認してから、再試行してください。  
発生場所 行:1 文字:1  
zsh: command not found: tsc  

## tscのコマンドが効かない時
typescriptを設置してもtscコマンドがうまく効かない場合があります。  
その時は下記のコマンドを入力すれば解決できす。  
```shell
npm install typescript -g
```