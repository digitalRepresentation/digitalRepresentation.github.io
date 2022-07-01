---
layout: post
title: "sourcetreeアカウント作成"
slug: sourcetree-アカウント-作成
comments: false
tags: [developer]
---
# ソースツリーアカウント追加
<img src="https://drive.google.com/uc?export=view&id=1Q4prhk1hbS4lVqR7cE5qjrgcIFjqE-eb" alt="ソースツリーでアカウント追加をする方法"  width="700" >

## sourcetreeの使う理由と意味
開発者がソースコードを管理するためにgitを使用します。  
gitはterminalで叩いて管理をするので、初心者がするのは難しいです。  
事前でgitの知識を慣れていたら、sourcetreeの機能もスムーズに使えます。  
sourcetreeはgitのGUI(Graphical User interface)のバージョンです。  
gitのpush, pull, branch等interface的にわかりやすく管理するのが可能です。  

## ソースツリーアカウント追加しましょう。
githubでrepositoryを作成したと仮定してご説明いたします。  
1. まず、sourcetreeを開きます。  
Remoteの雲アイコンを選択します。  
<img src="https://drive.google.com/uc?export=view&id=1exHMVhQpdGfOQR19hUJANTtrPmuyfW91" alt="sourcetreeメインページ"  width="700" >
      
2. 「アカウントを追加」をクリックします。  
<img src="https://drive.google.com/uc?export=view&id=15wpD4EX-cIkR4jdvCUolHhrXIs2_xasr" alt="sourcetreeアカウント追加"  width="700" >
      
3. ホスティングサービス、認証、ユーザー名を変更した後に「パスワードを再読み込み」をクリックします。  
ホスティングサービスは自分が利用しているのを選択してください。  
認証は基本的にBasicです。  
ユーザー名はgithubのメールアカウントではなく、githubの住所になるアカウントを入れてください。  
<img src="https://drive.google.com/uc?export=view&id=10LwnN59a8JH96rr10KUMumBk-Shex83v" alt="sourcetreeアカウント追加"  width="700" >
      
4. basic認証がかかってくるので、githubアカウントのパスワードを入力します。  
メールアカウントのパスワードではなくtokenを作ってtokenを入れます。  
tokenの作り方については別の記事で作成しましたのでご参考くださいませ。  
[githubのtoken生成方法](https://digitalrepresentation.github.io/2022/06/11/github-token-%E7%94%9F%E6%88%90/).  
<img src="https://drive.google.com/uc?export=view&id=1m-DdVhDz5Ei3zdNz4hAh0r2iccWV3fvz" alt="sourcetreeのbasic認証"  width="700" >
      
5. sourcetreeのアカウントの認証ができます。  
エラーメッセージになる場合がありますが、基本的にはtoken期限がなくなる場合と、  
githubログイン時のメールアカウントのパスワードを入れましたのでできない場合があります。  
<img src="https://drive.google.com/uc?export=view&id=16yrL-xxS3vlp0M3Yhnj5_GNCBvO7uVHg" alt="sourcetree認証完了"  width="700" >
      
## sourcetreeアカウント追加完了
アカウント追加が正常に完了できたらリモートリポジトリに自分のアカウントが登録されます。  
今からsourcetreeのリモートリポジトリが完了しましたので使えます。  
<img src="https://drive.google.com/uc?export=view&id=127-ZU4MCZWOB4USUIn2vOVILIx5Yrcqx" alt="sourcetreeアカウント追加完了"  width="700" >