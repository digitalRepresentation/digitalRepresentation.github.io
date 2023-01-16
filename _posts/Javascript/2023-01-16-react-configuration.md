---
layout: post
title: "Reactを設置して動作まで3分で説明します。"
slug: react-configuration
comments: false
tags: [javascript, developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Reduce of empty array with no initial value解決" width="700">

## Reactを設置して動作まで3分で説明します。

まず、node project managerを使うため、NodeJsを設置します。  
[NodeJs設置サイト](https://nodejs.org/ko/download/){:target="_blank"}

次はyarnを設置します。  
yarnはnpmより速度も速いし効率的なキャッシュシステムといろんな機能を提供します。  
npmを使いたかったら、yarnは設置をしなくても大丈夫です。  

### windowsの場合  
[yarn設置サイト](https://classic.yarnpkg.com/en/docs/install#windows-stable){:target="_blank"}
  
### macOSの場合
```terminal
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
  
Editorは便利なものを使用すれば問題ないですが、　　
ない場合はVisual Studio Codeを設置します。  
[VisualStudioCode設置サイト](https://code.visualstudio.com/Download){:target="_blank"}
  
設置ファイルは異常となります。  
次はプロジェクトを実行してみましょう。  

## reactを実行する方法
react projectを作るときはyarnのコマンドを使用します。  
```terminal
yarn create react-app project-name
```

npmを使うときは下記のようにコマンドを叩いてください。  
```terminal
npm init react-app project-name
```

プロジェクトが作成できたら、下記のコマンドを入力してください。  
```terminal
cd project-name
yarn start または npm start
```

成功した場合はターミナルに成功メッセージがでてhttp://localhost:3030が開きます。  
異常となります。  