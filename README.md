# plus-toast

一个轻量级的toast消息提示插件，帮你更好的使用消息提示和进行用户交互，各种类型消息，包括警告，错误，信息提示，确认等。还可以自定义html或者纯文本消息显示！

## How to use it?

```
npm install plus-toast
```

### How to use it in the project!

```
import PlusToast from 'plus-toast';

可使用参数
{
    duration: 4000,//表示显示时长，多久后关闭
    icon: "",//内置提供success，error，warning，info四个，也可以自定义图标，直接传入icon图标的svg或img
    type: "",// 表示消息显示类型：success，error，warning，info
    theme: "", //主体样式，light，dark，bubble主题样式
    closable: false,//是否可关闭，默认为false，为true时会出现一个关闭的X按钮，必须点击才能关闭，否则就是正常的依据显示时长后关闭
    position: "top",//表示显示位置，top，top-right,top-left,right,left,bottom,bottom-right,bottom-left,center
    animation: "slide", // 动画效果：'slide', 'fade',  'bounce'
    onlyOne: false,//是否只显示一次，多次点击只显示一次
    confirmMode: false,//是否为确认模式，确认模式可以和用户交互，会在消息下面显示确认和取消按钮
}

//简单使用方法，其他参数可以根据自己的需求使用
// show方法，常用的参数
PlusToast.show(
    "message",//为传入的文本消息或这可以是一段html代码
    {
        duration: 4000,
        icon: "",//内置提供success，error，warning，info四个，也可以自定义图标，直接传入icon图标的svg或img
        type: "light",// 设置黑暗/成功等显示类型：dark，success，error，warning，info，默认为light，light只是表明初始的样式是明亮主题
    }
);

// success方法，常用的参数
PlusToast.success(
    "message"//为传入的文本消息或这可以是一段html代码
);

// error方法，常用的参数
PlusToast.error(
    "message"//为传入的文本消息或这可以是一段html代码
);

// warning方法，常用的参数
PlusToast.warning(
    "message"//为传入的文本消息或这可以是一段html代码
);

// info方法，常用的参数
PlusToast.info(
    "message"//为传入的文本消息或这可以是一段html代码
);

// successM方法，移动端，常用的参数
PlusToast.successM(
    "message"//为传入的文本消息或这可以是一段html代码
);

// errorM方法，移动端，常用的参数
PlusToast.errorM(
    "message"//为传入的文本消息或这可以是一段html代码
);

// warningM方法，移动端，常用的参数
PlusToast.warningM(
    "message"//为传入的文本消息或这可以是一段html代码
);

// infoM方法，移动端，常用的参数
PlusToast.infoM(
    "message"//为传入的文本消息或这可以是一段html代码
);

// 注册登记特定方法，常用的参数,可以把注册登记的输入框传入
PlusToast.register(
    "message",//为传入的文本消息或这可以是一段html代码
    {
        duration: 4000,
        icon: "",//内置提供success，error，warning，info四个
        type: "light",// 设置黑暗/成功等显示类型：dark，success，error，warning，info，默认为light，light只是表明初始的样式是明亮主题
        position: "top",
    }
);

// 登录特定方法，常用的参数，可以把登录框相关的代码传入
PlusToast.login(
    "message",//为传入的文本消息或这可以是一段html代码
    {
        duration: 4000,
        icon: "",//内置提供success，error，warning，info四个
        type: "light",// 设置黑暗/成功等显示类型：dark，success，error，warning，info，默认为light，light只是表明初始的样式是明亮主题
        position: "top",
    }
);

// 显示确认取消消息框使用方法
PlusToast.confirm("确定要XXX吗？", {
    icon: "success",//主要有success，error，warning，info四个
    type: "success",//消息显示样式类型，success，error，warning，info，dark，light
    onConfirm: () => {
        // 用户点击确认后的操作
        console.log("用户点击了确认");
    },
    onCancel: () => {
        // 用户点击取消后的操作
        console.log("用户点击了取消");
    },
    cancelText: "不", // 自定义取消按钮文本
    confirmText: "是的", // 自定义确认按钮文本
});
...
```

### npm Docs

#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).