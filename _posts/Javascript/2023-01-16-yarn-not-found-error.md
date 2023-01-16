---
layout: post
title: "error Command “start” not found.のエラー解決"
slug: yarn-not-found-error
comments: false
tags: [javascript, developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Reduce of empty array with no initial value解決" width="700">

## error Command “start” not found.のエラー解決
Reactを実行しようと思ったら、reactがないというエラーが発生しました。  
こちらのエラーはターミナルで場所が間違えている時が主な理由です。  
なので、プロジェクトがある場所に移動してstartコマンドを叩いたら解決できます。  

```terminal
$ cd project-name
$ yarn start
```

解決できましたか。  
このように場所を指定してコマンドを叩くと解決できます。  