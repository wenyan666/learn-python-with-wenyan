## 预备周
- **认真看书**，如果你真的这么做了，根本不会有什么大问题，除非你只是假装认真看了。只要真的：
  - 安装python2
  - 用终端检查环境是否配置成功
  - 安装对应的文本编辑器并开始练习
  - 用终端检查你的练习是否正常运行
- [《Learn Python the Hard Way》的前17个小练习](https://github.com/wenyan666/wenyan-python)
- [练习笔记](https://github.com/wenyan666/wenyan-python/issues)
- 小节
在拿到书开始练习到12个练习的时候，没有遇到什么大问题，到后面会出现一些小问题，不过也都是单词拼错，把反括号写成了中文的，双引号另外一半忘记加上了这类的错误，根据报错信息提示很快就能改正。
 但是练习结束之后，留在脑袋里面的python模型并不完整，能提取出来的东西依旧很有限，于是开始思考：

> 为啥不试一下用六小时定理来练习？

- 就是看完书，然后不马上开始动手，在脑子里面预演，等合上书建个一定时间后再按照记忆或者自己的理解来敲代码练习？

很有趣。

你会发现，刚开始由速度带来的优越感都会消失，转而有越来越多的盲点。这是的hard way learn python才展示出它的hard。

这种方式也会迫使你放弃掉 **我很聪明** ，而转向 **我很努力** 。

聪明是自欺欺人，努力才是当下应该关注的不是么？


## CHO
配置环境在预备周的时候已经用Windows完成了预备周的任务，由于安装github客户端遇到了问题而中止了本地编辑，很不好的习惯，在ch0的时候正式配置好所有环境，包含软件环境和相关的工具。

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
有很多优秀的文本编辑器，如果有自己钟爱的，继续使用就行，如果没有，除了预备周《Learn Python the Hard Way》中提到的几款，开智卡包里面有很具体的的推荐方案：
>
#### Mac
- Machdown
- MWeb
- Atom
#### Windows
- MarkDownPad
- Atom
#### IOS
- EverMark
- iMWriter
#### Andriod
- 锤子便签
- MarkdownX

  - [我windows现在正在使用的atom](https://atom.io/)

### python2和python3的不同之处  

- 在《Learn Python the Hard Way》中选择了，选择5±2个练习用python3.x改写之，[这里是练习的代码](https://github.com/wenyan666/Py103/tree/master/Chap0/project)
- 官方信息源：[ the difference between Python 2 and 3](https://wiki.python.org/moin/Python2orPython3)，看文档看得非常吃力，主要英语阅读理解能力差再就是之前对python的了解也很基础，很多说到的不同点之前也没有用python2进行过练习。
- 挑选了3、5、12、15、17、19来进行改写，目前发现的主要差异（整本书19以后的练习都还没有敲，如果之前多敲一些，现在应该会发现更多的不同）：

名称 |python2 | python3
---|---|---
打印print | print"hello world"| print("hello world")
用户输入 | input()\nraw_input()| input()
整数除法 | 3/2 = 1| 3/2 = 1.5\n3//2 = 1

分别在挑选的ex3、12中发现了以上区别。
ex3
`
print ("I will now count my chichens:")

print ("Hens", 25+30//6)
print ("Roosters", 100-25*3%4)

print ("Now I will count the eggs:")

print (3+2+1-5+4%2-1//4+6)

print ("Is it true that 3+2<5-7?")

print (3+2<5-7)

print ("What is 3+2?",3+2)
print ("What is 5-7?",5-7)

print ("Oh,that's why it's Fslse.")
print ("How about some more.")
print ("Is it greater?",5>-2)
print ("Is it greater or equal?",5>=-2)
print ("Is it less or equal?",5<=-2)
print ("Hre is the new of branch?")

'''
python3源码默认使用utf-8进行编码，可以在注释中任意使用中文而无需在开头加上# coding:utf-8了；
原来的print""用print("")替代;
python3默认整除为浮点。为了和python2中得到一样的打印结果，必须将原来的/用//替代。
'''
`

ex12
'age = input("How old are you?")
height = input("How tall are you ?")
weight = input("How much do you weigh?")

print ("So,you're {0} old, {1} tall and {2} heavy.".format(age,height,weight))

'''
input 替代 raw_input
"{0} {1} {2}" .format(a,b,c)可替代"%x,%x,%y" %(a,b,c)
'''
'

### 可选任务：将个人教程发布以Gitbook形式发布
- 继续折腾中......
