---
layout: post
title: "typescriptのIntersection型とは"
slug: typescript-Intersection-summary
comments: false
tags: [javascript, developer]
---
## typescriptのIntersection型とは
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="typescriptのIntersection型の解説" width="600">

```jsx
interface Life {
  name: string;
  age: number;
}

interface People {
  address: string;
}
type LifePeople = Life & People;
```

&演算子はIntersection型で使われています。  
積集合なので共通でもっているプロパティーがないと思いますが、  
typescriptのIntersection型はinterfaceのプロパティー両方値を持っていないといけません。  

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
    

```jsx
const digitalPeople: LifePeoPle = {
  name: 'kong',
  age: 20,
  address: 'hokkaido'
};
```
このようにIntersection型を使う時は必ずinterfaceに書かれていたプロパティーを使わなければなりません。
  
  
