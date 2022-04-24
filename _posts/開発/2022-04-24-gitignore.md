---
layout: post
title: "gitで大事なファイルを隠したいときは"
slug: gitignore-mean
comments: true
tags: [developer]
---
gitで大事なファイルを隠したいときは  

## gitで隠したいファイルがあればどうするか。
gitに公開したくないファイルがある場合はgitignoreファイルを作成すれば、  
ファイルを隠すのが可能です。

## gitignoreとは
gitのバージョン管理ツールで特定なファイルを除外するリストを指定するファイルです。  

## gitignoreはどうやって作るの？
projectを作成する際に作れますが、  
もしかしてその時に作ってなくてもroot内に.gitignoreファイルを作れば大丈夫です。  
僕の場合はxamppの環境で作業をしているので、.gitignoreを作ってなくて、手でファイルを作成しました。  
<img src="https://drive.google.com/uc?export=view&id=11iWos6dQFHMLzomc2Z7aGabRp7l_b3HP"  width="700" height="370"> 

## gitignoreはなんで使うの？
gitignoreが必要な理由は製品のビルド情報やファイルのバックアップ情報、そして環境構築に必要なファイルでIDとPASSWORDを作成するファイルを隠すためにです。  
公開すれば厄介なファイルがかなりあると思いますので、  
おもにファイル名の先頭に「.」が入っているのはアップすればいけないです。  
例えば環境構築の「.env」ファイルとルーターファイルの「.htaccess」をアップしてリリースすると、  
ハッキングの恐れがあります。  

不明点がございましたら、コメントをお願いいたします。  
