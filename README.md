

**解决滚动元素内有大量dom，造成卡顿问题的方案**

clone 到本地  直接打开  example/index.html 可看到demo，可看到具体用法

[实现的dome效果在线查看][1]



 - 滚动加载，出现无限滚动时，可能给dom过多页面卡死
 - 滚动加载的组件，dom过多，销毁组件的时候也会出现卡死
 - 任何滚动的元素，内部元素过多，都会出现卡顿现象


**针对上面的问题，我们能否有什么优化的方案？**

代码实现了滚动dom中**‘可视区域展示’**的功能。如下图：
**我们做到，在非可视区域的dom，都暂时转存到内存中，为了防止抖动，也要实现占位功能**

![此处输入图片的描述][2]

实现后的效果如下，非可是区域，只有一个空的dom占位：
![此处输入图片的描述][3]


  [1]: http://g1024.top/vue-smart-scroll/example/index.html
  [2]: http://7xqd2y.com1.z0.glb.clouddn.com/keshi.jpg
  [3]: http://7xqd2y.com1.z0.glb.clouddn.com/gundong.gif
