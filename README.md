这是一个PHP后台cms的样例代码，比较粗糙，主要方便看原理，很方便自定义改为自己需要的类型

现在实现的功能有 ：数据库增、查，尚未添加 改、删，不过原理简单，其实就是执行Sql语句而已，
可以在前两个代码的基础之上修改即可。

服务端静态缓存：避免重复请求数据库，减少数据库压力。实际应用中设置个定时任务，定时更新缓
存即可。目前是手动设置了缓存超时时间，不依赖任何第三方的缓存服务。


demo代码结构介绍：

客户端代码调用到了两个接口
1.添加影片数据接口为 add.php
2.查询影片列表数据接口 为 getData.php

web访问方式，可直接运行init.html文件，此页面为添加数据页面，调用了add.php接口，代码很简单，一目了然
web访问没有做查询列表操作，可以直接调用getData.php获取列表的json响应，由于主要是APP端用，这就够了。

App访问方式，参考APPdemo代码即可。



部署方法：
    将cms文件夹直接丢到www目录下即可。（建议本地安装PHPstudy运行看效果）

注意事项：
    因每个人电脑环境不同，代码需要根据个人实际情况修改对应参数：
        dp.php中数据库的配置，修改为你自己的配置


（代码参考慕课网视频课而来）