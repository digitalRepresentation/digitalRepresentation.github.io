---
layout: post
title: "githubのtoken生成する方法"
slug: github-token-生成
comments: false
tags: [developer]
---
# githubトークン生成
<img src="https://drive.google.com/uc?export=view&id=1Q4prhk1hbS4lVqR7cE5qjrgcIFjqE-eb" alt="ソースツリーでアカウント追加をする方法"  width="700" >

## githubのトークン必要な理由
githubでID/PW形のBasic Authentication認証を禁止してID/Personal Access Token方式のToken Authentication認証を採択してあります。  
セキュリティー的な問題があるので、今後githubでpushをするときにtoken認証が必要となります。   
Password authentication is temporarily disabled as part of a brownout. Please use a personal access token instead.  
このエラーの内容を見た時はtokenを作って解決しましょう。  

## githubのtoken生成手順
1. githubの本人アカウントに入って、profileをクリックしてsettingに入ります。  
<img src="https://drive.google.com/uc?export=view&id=1ZXiprTaV58YGGIjVvNON6UxlN0YxqFzK" alt="githubのtoken生成手順"  width="700" >
      
2. 左側のメニューtabで一番下にDevelopersettingをクリックします。    
<img src="https://drive.google.com/uc?export=view&id=125_lfb4w0TGDjcFr2823ATZ0EPZa_G00" alt="githubのtoken生成手順"  width="300" >
      
3. 左のメニューでPersonal access tokenを選択して、Generate new tokenをクリックします。      
<img src="https://drive.google.com/uc?export=view&id=13K2RuMcaeV4mWoLAv6zHT8b0Z0sVcqus" alt="githubのtoken生成手順"  width="1000" >
      
4. 左のメニューでPersonal access tokenを選択して、Generate new tokenをクリックします。      
<img src="https://drive.google.com/uc?export=view&id=13K2RuMcaeV4mWoLAv6zHT8b0Z0sVcqus" alt="githubのtoken生成手順"  width="1000" >
      
5. NoteとExpirationとSelect scopeは全部入れます。  
github tokenのNoteは覚えやすい名前で目的を考えて記載します。  
Expirationはgithubのtokenの有効期限です。永久にもできますが、目的によって設定してください。有効期限が消えましたら再認証が必要となります。  
Select scopesは基本的に全部チェックする方が良いです。  
Generate tokenをクリックします。  

<img src="https://drive.google.com/uc?export=view&id=1KCvDibKXeuOZMWGj5hEaUlFBxJmjEEqE" alt="githubのtoken生成手順"  width="700" >
<img src="https://drive.google.com/uc?export=view&id=1B9zrYZhbYzqA__JXuKj06-4qKil_JNJp" alt="githubのtoken生成手順"  width="700" >
         

## githubのトークン発行完了  
githubのトークンが発行できました。  
こちらのトークン名は必ずメモしてください。  
tokenは追加はできますが、作ったtokenのtoken番号を確認するのはできません。  
<img src="https://drive.google.com/uc?export=view&id=1iUG5SdEF9Sif7hcsI-Sj34WaisCM9ZHa" alt="githubのtoken生成手順"  width="700" >