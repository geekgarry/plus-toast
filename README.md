# plus-toast

一个轻量级的toast消息提示插件，帮你更好的使用消息提示和进行用户交互，各种类型消息，包括警告，错误，信息提示，确认等。还可以自定义html或者纯文本消息显示！

## How to use it?

```
npm install plus-toast
```

### How to use it in the project!

```
import {showToast} from 'plus-toast';

//  全部的参数
showToast(
    "XXXX",//为传入的文本消息或这可以是一段html代码
    {
        duration: 3000, // 显示时长，单位毫秒，没有写时默认3000
        icon: "",//内置提供success，error，warning，info四个，也可以自定义图标，直接传入图标的svg或img
        theme: "light",// 设置主题黑暗/成功等显示背景：dark，success，error，warning，info
        closable: false,//是否可关闭，如果为默认为false，为true时会出现一个关闭的X按钮，必须点击才能关闭，否则就是正常的依据显示时长后关闭
        position: "top",//表示显示位置，top，top-right,top-left,right,left,bottom,bottom-right,bottom-left,center
        animation: "slide", // 动画效果：'slide', 'fade', 'bounce',默认为slide滑入滑出
    }
);
//简单使用方法，其他参数可以根据自己的需求使用
showToast(
    "message...",
    {
        duration: 3000
    }
);
...
```

### npm Docs

#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).