---
layout: post
title: "JSX 式には1つの親要素が必要です。解決方法"
slug: react-Adjacent-JSX-elements-must-be
comments: false
tags: [javascript, developer]
---
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="JSX式には1つの親要素が必要です。解決方法解決" width="700">

## JSX式には1つの親要素が必要です。解決方法
Reactを初めて使った人は上記のエラーと出会う可能性があります。  
まず、親要素が必要というのはdivタグ等を使わなければなりません。  
なぜ、Reactのコンポーネントで親要素に囲まれなければラナイかというと、  
はVirtual DOMでコンポーネントの変化を見る時に効率的に比較できるよう、  
コンポーネント内部は一つのDOM Tree仕組みになるべきというルールがあるからです。  
  
エラーになるソースコード  
```javascript
  return (
      <p>test</p>
      <h2>bye</h2>
  );
```

エラー解決するソースコード  
```javascript
  return (
      <div>
        <p>test</p>
        <h2>bye</h2>
      </div>
  );
```

## JSX式には1つの親要素が必要です。の解決方法2
「JSX式には1つの親要素が必要です。」のエラーを解決するためにはdivタグで囲まれると解決できますが、  
Fragmentという機能を使っても動作できます。  
  
```javascript
  return (
      <fragment>
        <p>test</p>
        <h2>bye</h2>
      </fragment>
  );
```

fragmentのタグは<>も表示できます。  
```javascript
  return (
      <>
        <p>test</p>
        <h2>bye</h2>
      </>
  );
```