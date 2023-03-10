# Handwriting_Recognition项目文档

### 一：项目简介

##### 1. 做了什么

**第一部分<算法实现>**：分别用 Numpy 和 TensorFlows 实现了二个版本的全连接神经网络，用 Mnist 数据集训练，将训练后的模型用真实手机拍照获得的手写数字图片进行识别，最后得到了不错的效果。

**第二部分<算法落地>**：将实现好的神经网路模型封装好，用PyQt5做了一个手写画板的界面，可以实现用户手写输入一个数字笔画后，自动识别转化为对应的数字。

##### 2. 代码结构

**src/numpy_demo**: 仅用 Numpy 库实现的一个全连接神经网路，无用到开源框架。

**src/tensorflow_demo**: 基于开源框架 TensorFlow 实现的全连接神经网络。

**src/data.rar**: 使用过程中需要用到的数据，运行源码前请先将该压缩文件解压至当前目录。

**dist**:  将 Numpy 版的神经网络，应用于手写画板，打包成的exe，无Python环境也可执行。

##### 3. 应用程序

打包后的 exe 程序过大，已经单独放至releases下。

------

### 二：项目预览

##### 1. 模型训练

​	把Mnist数据集划分为，训练集和测试集，下图是数字8的一些数据图片。

![](figures/data_8.jpg)

​	然后用模型训练，可以得到损失函数和模型在训练集和测试集上面的准确率。

​	![](figures/train.png)

##### 2. 模型验证

​	收集一份真实手写的手机拍照图片，如下所示：

![](figures/real_handwriting.jpg)

​	将手机拍照得到的手机图片，进行预处理后，作为未知数据集输入模型，得到对应的准确率：

![](figures/evaluate.png)

​	可见拍照获得的一百张手写图片中，只有一张手写识别出错了，错误率仅为1%。具体可看下图

![](figures/real_evaluate.png)

![](figures/error.png)

------

##### 3. 模型应用

​	将模型封装，应用于手写数字识别，用户手画一个数字，即可识别，桌面app示例如下：

![](figures/app1.png)

![](figures/app2.png)

