# 使用 —— 重新训练——保姆式教程

首先说明，这个库基本就是参考https://github.com/GaoPeng97/transformer-xl-chinese，非常感谢他们的工作，我就只是做了一些很小的改动，从而用起来更加方便。本人还没有仔细学习过里面的代码是怎样的，只是将代码调试跑通了。如果有问题，请稍等我过段时间看完后，会再写一篇更详细的说明，还望各位包含。

注意：一定要注意好各个模块的版本

## 1、复制git

直接在Terminal中，运行下方命令即可：

git clone https://github.com/Mateguo1/writing_robot.git

## 2、数据集：

自定义数据，小说文字格式复制

**！！！注意：**

（1）这里建议直接将内容复制到 ./data/doupo/train.txt（训练文件）和 /data/doupo/valid.txt (测试文件) 中去，不然编码可能会很烦。

（2）不太建议更改doupo文件夹名字或是创建一个新的文件夹，因为如果这样的话，你要改很多地方的名字很麻烦，但你非要这么做的话，孩子也没办法，还有换的话一口气都换掉，不然很麻烦。

## 3、处理数据：

这里你还是不需要做任何操作，都已经帮你改好。如果出错的话，建议检查下文件路径，一般都是这个问题。

直接在Terminal中，运行下方命令即可：

bash ./writing_robot/scripts/doupo_base_gpu.sh train_data

## 4、训练模型：

这里你还是不需要做任何操作，都已经帮你改好。如果出错的话，建议检查下文件路径，一般都是这个问题。

直接在Terminal中，运行下方命令即可：

bash ./writing_robot/scripts/doupo_base_gpu.sh train

## 5、测试结果：

这里你依旧是不需要做任何操作，都已经帮你改好。如果出错的话，建议检查下文件路径，一般都是这个问题。

直接在Terminal中，运行下方命令即可：

bash ./writing_robot/scripts/doupo_base_gpu.sh inference

这样结果出来后，你就可以得到新的内容啦

