## CHap0

### 配置环境
手里只有windows，然后想折腾linux虚拟机，后来还是决定入手Mac。环境选择上强推OS X，其次是linux，如果始终坚持要用windows，那就做好迎接九九八十一难的准备。
- **软件环境**
  - Windows环境无需多配置，预备周看书就知道在电脑里面找到对应的地方基本就没问题。
  - Linux虚拟机安装只需两步：
  1. [一手信息源官网下载VMware Virtualization](http://www.vmware.com/products/workstation/workstation-evaluation.html)，不懂英语新手也可以直接百度，百度软件中心已经有12.5.2版本，直接下载安装即可，下载完后傻瓜式安装，密锁问题有条件的走正规渠道，没条件的百度可以帮到你；
  2. [下载ubuntu](https://www.ubuntu.com/download/desktop)
  两者怎么配合记得google一下，当然了，google不是必须，很多时候百度一下或许能得到更加快捷的答案。 **一定善用工具。**
  - OS X，Mac还在路上，听说巨简单，到手了再研究。

- **github客户端安装**
  - 第一步：[下载github客户端](https://desktop.github.com/)
  - 第二步：把github-windows.s3.amazonaws.com 设置为信任站点，如果不知道怎么设置，请看[这里](https://www.zhihu.com/question/21623581/answer/67127382)
  - 第三步：傻瓜式安装github客户端
  - **重要提醒：** 有时候正确设置了信任站点也不一定会安装成功，看点子和运气，多尝试几次，比如我就是在前一天晚上尝试了不知道多少次都没有成功，而在第二天早上再尝试的时候一次性就完成。

- **文本编辑器**
  - 有很多优秀的文本编辑器，如果有自己钟爱的，继续使用就行，如果没有，除了预备周《Learn Python the Hard Way》中提到的几款，开智卡包里面有很具体的的推荐方案。
  
### python2和python3的不同之处  

- 在《Learn Python the Hard Way》中选择了，选择5±2个练习用python3.x改写之，[这里是练习的代码](https://github.com/wenyan666/Py103/tree/master/Chap0/project)
- 官方信息源：[ the difference between Python 2 and 3](https://wiki.python.org/moin/Python2orPython3)，看文档看得非常吃力，主要英语阅读理解能力差再就是之前对python的了解也很基础，很多说到的不同点之前也没有用python2进行过练习。
- 挑选了3、5、12、15、17、19来进行改写，目前发现的主要差异（整本书19以后的练习都还没有敲，如果之前多敲一些，现在应该会发现更多的不同）：

名称 |python2 | python3
---|---|---
打印print | print"hello world"| print("hello world")
用户输入 | input()、raw_input()| input()
整数除法 | 3/2 = 1| 3/2 = 1.5 、 3//2 = 1


### 可选任务：将个人教程发布以Gitbook形式发布

- [未完成的gitbook](https://wenyan666.gitbooks.io/learn-python-with-wenyan/content/)

### 总结
- 不要一知半解，不要只停留在不求甚解的阶段
- 任务要及时完成，不然疑惑会越来越多直到堆积到你不能前进
- 不要试图在学习上耍小聪明
