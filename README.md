# InputHideBottom
<BR>输入时顶起键盘的处理案例，项目上线案例<BR>
<BR>网上有很多的例子，但没有统一的解决方案，之后研究一下，发现键盘顶起后，原有的高度是有变化的，
设置隐藏的样式也很重要<BR>
 
<BR>scrollHeight: 获取对象的滚动高度。 <BR>
<BR>scrollLeft:设置或获取位于对象左边界和窗口中目前可见内容的最左端之间的距离 <BR>
<BR>scrollTop:设置或获取位于对象最顶端和窗口中可见内容的最顶端之间的距离 <BR>
<BR>scrollWidth:获取对象的滚动宽度 <BR>
<BR>offsetHeight:获取对象相对于版面或由父坐标 offsetParent 属性指定的父坐标的高度 <BR>
<BR>offsetLeft:获取对象相对于版面或由 offsetParent 属性指定的父坐标的计算左侧位置 <BR>
<BR>offsetTop:获取对象相对于版面或由 offsetTop 属性指定的父坐标的计算顶端位置 <BR>
<BR>event.clientX 相对文档的水平座标 <BR>
<BR>event.clientY 相对文档的垂直座标 <BR>
<BR>event.offsetX 相对容器的水平坐标 <BR>
<BR>event.offsetY 相对容器的垂直坐标 <BR>
<BR>document.documentElement.scrollTop 垂直方向滚动的值 <BR>
<BR>event.clientX+document.documentElement.scrollTop 相对文档的水平座标+垂直方向滚动的量<BR>
 
<BR>1.开始时<BR>
<BR>![image](https://github.com/MbsGood/InputHideKb/blob/master/1.png)<BR>
<BR>#切换的样式设置<BR>
<BR>
 .hasKb {
    opacity: 0;
    pointer-events: none;
  }
  <BR>
    <BR>
  .noKb {
    opacity: 1;
    pointer-events: auto;
  }
 <BR>
<BR>2.处理后，完美解决<BR>
<BR>![image](https://github.com/MbsGood/InputHideKb/blob/master/3.png)<BR>
<BR>3.代码 （有更好的方案可交流扣扣@382519962）<BR>
<BR>![image](https://github.com/MbsGood/InputHideKb/blob/master/2.png)<BR>
