# Keras-Leraning
这是一个自学Keras的笔记，记录了常用的方法和一些坑，方便以后回溯

所有文件在如下环境中进行了测试：  
Tensorflow-GPU==2.4.0  
CUDA==11.0  
cuDNN==8.0  

【小贴士】：安装完一个新版本的CUDA和cuDNN后一定要重新启动，否则会发现无论安装什么版本的都会报错，我在这上面耗费了2天多时间。
           CSDN上很多文章都忘了写需要重启这一项，切记切记！！！  
           不知道版本对应的下面是连接：  
           https://tensorflow.google.cn/install/source_windows

------------------------------

## 食用顺序
Quick Start -->  Save and Load --> Tensorboard --> Mutil GPU --> Advance  

此外，Help Manule 中有损失函数loss，评价标准metrics，优化器optimizer，模型编译compile，常用数据集datasets的快速查询表格。  

对于初学者而言必须将Quick Start中的代码完完全全敲上2遍以加深印象，进阶的读者可以直接从Advance开始阅读。

------------------------------

## Quick Start：
该文件夹用于快速上手，并不会非常详细地讲解神经网络各层的意义及作用，仅展示了如何使用Tensorflow.keras下的工具快速搭建一个神经网络模型。  
该文件夹下并不会考虑保存和加载模型的事宜，因为这些文件的初衷是让新手快速上手，但实际上保存一个训练好的文件 & 从硬盘中加载这个文件是一个十分重要的内容，毕竟所有人都不希望使用模型的时候每次都要重新训练。

文件夹下面包含了数个案例，建议一个一个仔细看，一定要上手敲！  
从我带的学生表现上来看，很多细节如Conv2D()函数中的参数遗漏只有在上手敲的时候才会被发现，这些案例也是我给他们讲过的。  
  
如何检测自己是不是熟练掌握了快速搭建模型的技能，我这有几个要素用于自查：  
* 1.随手绘制一个层数在8-15层的网络结构及各层参数，能在15min之内搭建好并通过plot_model检测。   
* 2.能用def自定义结构，尽量避免冗余代码。  
* 3.对于不同种类问题知道使用什么loss、metrics、激活函数。  
【注】plot_model是一个很好的函数，如果你的模型结构有错误，用这个函数一定会报错。特别是后面用到大量自定义层的时候，很多问题在调用前不会显露出来。  

在这个文件夹下的代码不用太在意模型性能，因为很多数据都是用numpy随机生成的。


----------------------------------

## Help Manuel:
该文件夹下存放了loss，metrics，optimizer，datasets，compile，callbacks的常见操作，在使用过程中不清楚的可以用来快速查找，对于初学而言足够折腾了。  
在Quick Start中callbacks不常见，但这个却是非常好用的功能，可以用来控制模型的计算和自动化。  


