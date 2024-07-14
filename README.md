# plus-toast

一个轻量级的toast消息提示插件，帮你更好的使用消息提示和进行用户交互，各种类型消息，包括警告，错误，信息提示，确认等。还可以自定义html或者纯文本消息显示！

## How to use it?

```
npm install plus-toast
```

### How to use it in the project!

```
import {showToast} from 'plus-toast';

//使用方式
showToast({
    "XXXX",//为传入的文本消息或这可以是html标签元素
    {
        duration: 3000, // 显示时长，单位毫秒，没有写时默认3000
        type: '', //success, error, warning, info
    }// ... 其他选项
});
...
```

### npm Docs

#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).
