比起前两周的毫无头绪，这周已经开始有了自己的节奏和思路，不再像无头苍蝇一样焦虑不安。

## 这次作业的执行节奏如下：
#### step1：
**重复阅读chap2卡包**直到明确这期任务及知识点：tkinter、OOP（面向对象编程）、GUI，然后针对知识点去学习。

#### step2：
开始关于本次任务的**事实性知识**（这是在《为什么学生不喜欢上学》中学到的新名词哈哈哈哈）学习！ 如：tkinter中label、button、entry、grid等的使用                                                     
- **首选一手信息源：** 卡包提供弄的信息源完全可以包含完成这期任务的所有知识点和方法，英语阅读能力好的，跟着卡包提供的线索走，很快就能找到思路。
- **Google翻译辅助阅读一手信息源：** 对于英语阅读理解能力不咋的的，也可以配合用chrome的自带Google翻译对照着来看，翻译会有出入，逐渐对照还是可以意会到其意思的。
- **中文信息源：** 如果觉得对着Google翻译看太费劲，且理解起来不顺畅，其实也还是有不错的中文资源的：
    - 《笨方法学python》能吃透里面提到的每一个知识点...这次chap2的任务需要 **反复通读练习40。**
    - python基础：[python基础教程](http://www.runoob.com/python/python-tutorial.html)
    - tikinter：[Tkinter详解](http://blog.csdn.net/jcodeer/article/category/339279/2)（这个资源是@yxlbetty的教程里面看到的）

#### step3：
整合看过的所有资料，然后开干！最开始一定会懵逼的，别担心，直接开干是最好的选择，只要你不提前崩溃行动瘫痪，文本编辑器、cmder/atom永远都会陪你玩儿，不管你犯了多么愚蠢的错误，他们永远都不会歇菜，永远都处于待命状态！

![picture1](https://cloud.githubusercontent.com/assets/24456998/22180719/731af5c8-e0b3-11e6-942c-4944c3371d4b.jpg)

## 我是这样开始最小行动的
1. 调用tkinter整一个空白窗口出来：
    ```
    from tkinter import *
    root = Tk()
    root.mainloop()
    ```
2. 尝试着把按钮啥的都加进去:
    ```
    # coding:utf-8
    from tkinter import *
    root = Tk()

    Frame(root,height =300, width = 300).grid()
    
    v = StringVar()
    Label(root,text = warm_prompt, justify = 'left').grid(row = 0,sticky = 'n')
    v.set = ( """
    温馨提示：
    直接输入城市即可查看该城市的天气情况~
    点击帮助，可查看帮助文档
    """)
    
    e = StringVar()
    Entry(root, fg = 'gray75', textvariable = e).grid(row = 10, sticky = 'w')
    e.set('输入城市名查询天气')

    button1 = Button(root, text = '查询'，anchor = 'se').grid(row = 10, column =0)
    button2 = Button(root, text = '帮助', anchor = 'se').grid(row = 10, column =1)
    button3 = Button(root, text = '历史记录', anchor = 'se').grid(row = 10, column =2)
    button4 = Button(root, text = '退出', bd = 4, anchor = 'se').grid(row = 10, column =3)

    root.title('天气助手')
    root.mainloop()
    ```
3. 试着结合现在的结构把chap1的代码结合进来，这个过程需要看chap1是以哪种方式完成的，如果各个功能都是def单独完成的，那么就可直接调用，调用方法为：
    ```
    import file_name  #(以.py结尾的文件名)
    file_name.function_name()
    file_name.variable_name
    ```
    如果不是用def单个定义的，那么就用上周的思路，试着和tk里面的控件结合在一起。
    过程会比较曲折，不要害怕敲错了

4. 最后慢慢尝试把所有的这些东西都放在类`class`里面：
    ```
    # coding:utf-8
    from tkinter import *
    root = Tk()
    class name_as_you_like(object):
        def __init__(self, org):
        .
        .
        new_variable = name_as_you_like()
    root.mainloop()
    ```
    类（class）就是新建了一个有多种属性的对象，但是这个类不能直接拿就用，而是将类当做一个“蓝图”，拷贝一个和类有相同属性的变量（new_variable），新建的对象就赋给给了新的变量，这就相当于当你像调用函数一样调用类的时候， Python 完成这个“迷你 import”的过程。
    
    **不断试错，不怕试错，掉坑了大不了爬出来。当然了善用工具善于总结比便于高效爬坑也是很重要的，毕竟......还有那么多坑等着你去爬呢......**
    

## 总结
- **静下心来学习：** 这个过程坑很多，但是你只要不停下来，基本上所有的问题都会得到解答，不管是用百度，还是Google，只要你静得下心学习，总会看到别人是怎么从这个坑里爬出来......然后掉进另外一个坑的-_-。

- **善用工具：StackOverflow** 在类里面定义enter的时候，就算你读了关于entry的文字介绍，一开始也不知道怎么定义一个enter，过程中可能会按照定义其他函数的方式org(self)是行不通的，程序会告诉你: `enter() takes 1 positional argument but 2 were given`
把这个copy去Google一下，通过StackOverflow就会发现需要在后面加一个event，果然就真的可以了。

- **善用py103同侪资源** 对了，再不济，还有同学早就提交的作业可以参考呢，别以为读懂大家的代码容易，看懂并理解也是一种本事。之前对直接学习同侪的代码比较忌讳，且心理负担也比较大，但是后来想想，我上网找教程其实也是在看别人的代码，把优秀同侪的作业当做教程之一来看又有何不可？

- **关注课程issue：** 比如，在Mac种tk不能输入中文的问题，就有人完美解决了[OSX中的 Tk GUI无法输入中文的问题](https://code661.github.io/2017/01/20/a-problem-about-Tk-input_chinese/)
    - 下载[ActiveTcl 8.5.18.0](http://www.activestate.com/activetcl/downloads)并安装
    - 重装python3更新tk库 / 或者直接在终端分两步输入`pyenv uninstall 3.5.2`、`pyenv install 3.5.2`即可

---
附上这期代码：[weather_helper](https://github.com/wenyan666/Py103/blob/master/Chap2/project/weather_heoper.py)

