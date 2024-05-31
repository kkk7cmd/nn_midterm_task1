# nn_midterm_task1

## 代码运行前准备
### 数据集下载
将CUB_200_2011数据集下载到统一目录下，并将以下目录进行更换，data_dir = 'D:\FDU\Course\DeepLearning\midterm\CUB_200_2011\CUB_200_2011'

### 参数设置
针对两个超参数的调整分别在如下两个位置进行修改，对于输出层学习率设置，在下面代码中的0.01处修改

`optimizer = optim.SGD([
    {'params': model.fc.parameters(), 'lr': 0.01}, 
    {'params': params_to_update, 'lr': 0.001}  
], momentum=0.9)`

对于训练轮数超参数的修改，在下面代码修改

`epochs = 20`

### 预训练设置
下面参数中设置为True为预训练模型，设置为False为随机初始化模型

`model = resnet18(pretrained=False)`

## 代码运行
直接运行ipynb文件中除最后一个cell之外的所有cell即可完成模型的训练

对于参数的调整可以通过最后一个cell运行

runs目录存储了tensorboard训练过程记录，其中子目录的命名格式为birds_experiment_epoch_learningRate，分别代表训练轮次和学习率，当前目录下，运行tensorboard --logdir=./runs可以查看训练过程

