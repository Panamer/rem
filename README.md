# rem
rem布局适配各种移动端

研究一天rem布局，试图寻找一种完美的rem写法，不限时框架（vue，react）

然而，并没有找到

js实现rem的方法：原理 clientWidth/dw = 实际显示/设计稿尺寸

例如：

在vue中可以用css预编译处理，比如sass和less，也可以写一个loader来处理。

一种完整的实现流程：媒体查询实现不同的屏幕尺寸对应不同的font-size，然后通过sass封装px2rem，width：px2rem（60）就可以了

部分公司也用flexable.js      lib-flexible

不巧，lib-flexible这个过渡方案已经可以放弃使用。建议大家开始使用viewport来替代此方案，vw的兼容方案可以参阅《如何在Vue项目中使用vw实现移动端适配》一文。

于是就看了一遍vw实现移动端适配,决定尝试一番

目前项目里的实现方式是：媒体查询处理不同机型，在sass里定义$font=37.5  width: 65rem/$font


