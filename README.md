# InputHideKb
<BR>输入时顶起键盘的处理案例，项目上线案例<BR>
<BR>网上有很多的例子，但没有统一的解决方案，之后研究一下，发现键盘顶起后，原有的高度是有变化的，
设置隐藏的样式也很重要<BR>
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
<BR>2.处理后<BR>
<BR>![image](https://github.com/MbsGood/InputHideKb/blob/master/3.png)<BR>
<BR>3.处理方案 （有更好的方案麻烦交流一下扣扣@382519962，不明白的也可咨询）<BR>
<BR>![image](https://github.com/MbsGood/InputHideKb/blob/master/2.png)<BR>
