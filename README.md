# 纯CSS飞机窗风格的toggle控件
纯CSS飞机窗风格的toggle控件
关于此动画中的一些知识点：
1.vh的用法？
vw：1vw等于视口宽度的1%。
vh：1vh等于视口高度的1%。
vh and vw：相对于视口的高度和宽度，而不是父元素的（CSS百分比是相对于包含它的最近的父元素的高度和宽度）。1vh 等于1/100的视口高度，1vw 等于1/100的视口宽度。
比如：浏览器高度950px，宽度为1920px, 1 vh = 950px/100 = 9.5 px，1vw = 1920px/100 =19.2 px。

2.:root的用法
:root 选择器匹配文档根元素。
在 HTML 中，根元素始终是 html 元素。
由于下文要用到字号，所以采用变量，在下文若使用font-size,则直接var(font-size)即可

3.radial-gradient(orange,orangered)的用法
这个属性为径向渐变.

4.若要在checkbox 被checked，则是
。toggle:checked ~ .window .curtain{
  修改属性.
}

5.塑造动画效果
.clouds span{
  animation: move 4s linear infinite;
}
@keyframes move{
  from {
    left:-150%
  }
  to{
    left:150%
  }
}

6.calc的用法
可把百分比与具体的数值进行加减乘除
如：calc((100% - 1.6em)/2)

7.transform:scale(2);
对于对应类名的DOM放大两倍

8.animation-delay" 2s
延迟2秒后再执行
