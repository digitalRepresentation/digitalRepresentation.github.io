---
layout: post
title: "Invalid event handler property `onclick`. Did you mean `onClick`?のジャバスクリプト"
slug: react-input-onclick-error
comments: false
tags: [javascript, developer]
---
## Invalid event handler property `onclick`. Did you mean `onClick`?のjavascriptエラー
<img src="https://drive.google.com/uc?export=view&id=1u7BSBIt1dMa6djlVbF-VmF72fTZ1X3TL" alt="Invalid event handler property `onclick`. Did you mean `onClick`?のジャバスクリプト" width="600">
Reactのinputのonclick, onchangeはHtmlと違くてcamelCaseにかけなければなりません。  
なので、全部小文字にするとエラーになります。
上記のエラーはonclickではなく、onClickだと書いたらエラーの解決ができます。

```javascript
<input
    type="submit"
    onclick={
        (e) => {
            console.log(e);
        }
        }
    />
```