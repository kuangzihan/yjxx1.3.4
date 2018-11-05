#优化内容如下：

##1、页面跳转交互优化

跳转页面加载圆圈优化，跳转页面如页面在加载并不会影响返回等操作（包括侧滑返回）

![展示图](https://raw.githubusercontent.com/kuangzihan/yjxx1.3.4/master/1.gif)

<br>
##2、webView优化：


自测webView在未获取相册权限，长按图片保存相册会导致crash。<br>
webView并不能识别网页自带的长按功能，所以针对这个问题的优化是，禁用网页长按识别，在webview长按img标签<通过js代码只识别img标签>，则弹出alert。包括看图模式、保存相册、复制图片链接。其中看图模式大致实现方式为获取web上所有的img标签，并通过dom获取src进行图片展示。

![展示图](https://raw.githubusercontent.com/kuangzihan/yjxx1.3.4/master/2.gif)


<br>
##3、图片查看器优化：
对原有图片查看器进行替换（整体替换，包括全部使用图片查看器功能页面），目前实现效果类似微信的图片查看器。<br>
图片查看器可查看长图

![展示图](https://raw.githubusercontent.com/kuangzihan/yjxx1.3.4/master/3.gif)


##4、商品详情优化:
商品详情轮播图及图片详情支持查看大图

![展示图](https://raw.githubusercontent.com/kuangzihan/yjxx1.3.4/master/4.gif)



##5、保存相册流程优化，
如a用户已明确拒绝相册权限时，添加友好提示引导。

![展示图](https://raw.githubusercontent.com/kuangzihan/yjxx1.3.4/master/5.gif)




###还包括其他性能及细节方面的优化，减少app启动时间，webView白屏时间减少等。