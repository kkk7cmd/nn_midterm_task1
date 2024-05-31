# nn_midterm_task1

## 代码运行前准备
### 数据集下载
将CUB_200_2011数据集下载到统一目录下，并将以下目录进行更换，data_dir = 'D:\FDU\Course\DeepLearning\midterm\CUB_200_2011\CUB_200_2011'

### 参数设置
针对两个超参数
`optimizer = optim.SGD([
    {'params': model.fc.parameters(), 'lr': 0.01},  # 高学习率仅适用于全连接层
    {'params': params_to_update, 'lr': 0.001}       # 低学习率适用于其余层
], momentum=0.9)`
