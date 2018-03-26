### 小清新的导航页面

简约、扁平化的 UI 界面深受大众的喜爱。

该导航页面特色在于用户敲击键盘上的字母，即可快速导航至与该字母相关联的页面，当然，用户可以自定义相关联的页面。

[原链接](http://captaininphw.xyz/browser-navigation-page/index.html)
---
修复BUG ie兼容不了Object.values，需添加一个判断属性 

```
//兼容IE浏览器 Object.values兼容不支持它的旧环境IE
if (!Object.values) Object.values = function(obj) {
    if (obj !== Object(obj))
        throw new TypeError('Object.values called on a non-object');
    var val=[],key;
    for (key in obj) {
        if (Object.prototype.hasOwnProperty.call(obj,key)) {
            val.push(obj[key]);
        }
    }
    return val;
}
```
