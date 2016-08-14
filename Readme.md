#Ghost的Dockerfile
本dockerfile简介:简单的配置ghost blog 0.9.0，目前是最新版本，并且可以避免网络上其他dockerfile把你的静态链接url指定到localhost或者其他无法访问的网址的bug。**更重要的是，还附赠一篇超详细的网站搭建教程，小白都能撘网站。你是小白的原因就是你不敢试**
##使用Ghost建网站
全程可以在手机上完成，如果可以有平板或电脑，可能会更好
###1.Fork
如果你没有GitHub账号，请先注册
然后将此repo `fork`到GitHub账号下
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-13-41-36----.png)
PS:手机请点击页面下方切换到电脑版
###2.修改config.js
将其中的中文改成`http://你想要的子域名.daoapp.io`（如果你没有自己的顶级域名或者不想使用）或者`http://你自己的域名`（前提是你已经拥有了这个域名）
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-13-44-50----.png)
然后进行`commit`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-13-45-54----.png)
###3.在daocloud注册
[点击这里](https://account.daocloud.io/signup)打开注册界面
建议直接通过`github`注册，这样接下去就不用绑定了
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-13-49-53----.png)
完成注册
###4.绑定GitHub，进行代码构建
打开第一个按钮
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-02-17----.png)
选择`创建新项目`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-03-46----.png)
填写`项目名称`，绑定github后点击右上角旋转按钮`同步数据`，在你的github头像下方的下拉框选择`Dockerfile-for-ghost`*一定要选择！*，像这样
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-06-45----.png)
创建完成后，先选择`master`分支，再点击`手动构建`
等待五分钟左右，显示构建成功了
###5.部署你的ghost
构建成功后，点击`镜像仓库`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-15-08----.png)
点击`部署`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-16-13----.png)
再点击`部署最新版本`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-19-06----.png)
*一定要选择`2x`!*不然部署完成后内存不足
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-21-03----.png)
点击`基础设置`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-22-24----.png)
下一页请不要改动任何数据，直接点击`立即部署`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-23-43----.png)
###6.进行最后的设置
>如果你修改config.js时填写的是像`http://hjl.daoapp.io/`这样的域名

请记下`//`和`.daoapp`这一段，例如`hjl`
然后填写在文本框中
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-29-08----.png)
点击`保存更改`并等待一段时间

>如果你在编辑config.js时填写的是像`http://23333.ga`这样的域名（前提是你已经拥有了这个域名）

请`绑定自有域名`
![](http://hjl.daoapp.io/content/images/2016/08/2016-08-14-14-34-15----.png)
如果你有域名，想必你应该会使用，只要把域名cname到系统生成的形如`46ldx2gv90.daoapp.me`的地址就可以了
###7.配置ghost
访问你的域名再加上`/ghost`，例如`http://hjl.daoapp.io/ghost`

PS:这时服务器需要读写大量数据，可能较慢

PS:由于我已经设置好了，所以此时不提供截图

在第一个屏幕点击绿色按钮，在第二个屏幕的四个文本框内依次输入`你的邮箱` `你的用户名` `设置密码` `blog网站标题`完成后点击绿色按钮。第三个页面是邀请小伙伴，输入小伙伴的邮箱并点击绿色按钮，如果不想邀请，点击绿色按钮下面的一行灰字

完成后你就进入你的网站啦~
##教程到此截止
#####后记
1.我自己的网站为[http://hjl.daoapp.io/](http://hjl.daoapp.io)
2.这篇文章全手打，大约打了一个多小时
3.如果本dockerfile有任何真正的bug，请在github上给我提交反馈或者在我的网站上留言
