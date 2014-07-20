# jquery-scrollable [![spm version](http://spmjs.io/badge/jquery-scrollable)](http://spmjs.io/package/jquery-scrollable)

AUTHOR WEBSITE: [http://ydr.me/](http://ydr.me/)

jquery.fn.scrollable 无限滚动

**五星提示：当前脚本未作优化、未完工，请勿用在生产环境**

__IT IS [A SPM PACKAGE](http://spmjs.io/package/jquery-scrollable).__



#DOM
```
ul#demo>li*n
```



#USAGE
```
var $ = require('jquery');
require('jquery-scrollable')($);

// 1、初始化
$('#demo').scrollable();

// 2、直接跳转到第几个
$('#demo').scrollable(index[,duration][,callback]);

// 3、播放
$('#demo').scrollable("play");

// 4、暂停
$('#demo').scrollable("pause");

// 5、上一个
$('#demo').scrollable("prev");

// 6、下一个
$('#demo').scrollable("next");
```



#OPTIONS
```
$.fn.scrollable.defaults = {
    // 列表选择器
    listSelector: "li",

    // 容器宽度，超过隐藏
    width: "auto",

    // 容器高度，超过隐藏
    height: "auto",

    // 滚动方向
    direction: "top",

    // 每次滚动的项目数量
    // 如果为1，则每次滚动1个，暂停的时候会是某一个项目的结尾
    // 如果为0，则无缝滚动，暂停的时候可能会是某一个项目的中间
    scrollCount: 1,

    // 延迟时间
    delay: 2000,

    // 动画时间，如果滚动数量为0，则滚动全部数量的动画时间
    duration: 678,

    // 是否自动播放
    isAutoPlay: true,

    // 是否鼠标悬停暂停
    isHoverPause: true,

    // 变化之前回调
    // this => element
    onbeforechange: emptyFn,

    // 变化之后回调
    // this => element
    onafterchange: emptyFn
};
```
