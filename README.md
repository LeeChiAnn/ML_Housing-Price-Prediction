# 波士顿房价预测教学案例

## 一、课程目标

本案例面向机器学习与深度学习入门教学，围绕“房价预测”这一经典回归问题展开，帮助学生理解以下内容：

1. 数据预处理方法
2. 线性回归与神经网络的基本思想
3. 训练过程中的损失函数与梯度下降
4. 如何使用框架简化模型实现
5. 如何通过可视化分析模型效果

本项目提供两种实现路线：

- NumPy 版：适合理解底层计算逻辑
- Paddle 版：适合理解框架式开发方式

---

## 二、项目文件说明

### 1. NumPy 版本

- `work/1-2-build_neural_network_using_numpy.py`
- 适合学习：
  - 手工实现前向传播
  - 计算损失函数
  - 反向传播与参数更新
  - 自定义训练循环

### 2. Paddle 版本

- `work/1-3-build_neural_network_using_paddle.py`
- 适合学习：
  - 飞桨框架使用方式
  - `Linear` 层、优化器和损失函数
  - 自动求导与模型训练

### 3. Notebook

- `main.ipynb`
- 适合课堂讲解和 AI Studio 演示
- 运行后可直接查看训练过程与可视化结果

---

## 三、数据说明

本项目使用的是波士顿房价数据集，数据文件位于：

- `work/housing.data`

数据共有 14 列，前 13 列为特征，最后 1 列为房价标签（MEDV）。

其中包括：

- CRIM
- ZN
- INDUS
- CHAS
- NOX
- RM
- AGE
- DIS
- RAD
- TAX
- PTRATIO
- B
- LSTAT
- MEDV

---

## 四、如何运行

### 方式一：直接运行脚本

#### 1）运行 NumPy 版本

```bash
python work/1-2-build_neural_network_using_numpy.py
```

#### 2）运行 Paddle 版本

```bash
python work/1-3-build_neural_network_using_paddle.py
```

### 方式二：在 Notebook 中运行

打开 `main.ipynb`，按单元格依次执行即可。

---

## 五、学生可以修改的参数

在脚本开头，已经预留了核心训练参数，学生可以直接修改：

```python
EPOCH_NUM = 10
BATCH_SIZE = 10
LEARNING_RATE = 0.01
```

### 参数建议

- `EPOCH_NUM`：训练轮数
  - 轮数过少，模型可能欠拟合
  - 轮数过多，训练耗时增加

- `BATCH_SIZE`：每批样本数
  - 批量过大，训练稳定但更新较慢
  - 批量过小，梯度噪声较大

- `LEARNING_RATE`：学习率
  - 太大可能震荡
  - 太小则收敛缓慢

学生可以尝试修改为：

```python
EPOCH_NUM = 20
BATCH_SIZE = 20
LEARNING_RATE = 0.05
```

观察不同设置下的训练结果和图像变化。

---

## 六、训练完成后会自动生成什么图

程序训练结束后，会自动保存图片到 `generated_figures/` 文件夹中，默认生成三张图：

1. `loss_curve.png`
   - 展示训练过程中的损失值变化
   - 用于观察模型是否收敛

2. `prediction_vs_actual.png`
   - 展示真实房价与预测房价的对比
   - 用于分析模型拟合效果

3. `weight_distribution.png`
   - 展示模型权重的分布情况
   - 用于理解模型参数是如何变化的

这些图片可以直接用于课堂展示、作业提交和实验报告。

---

## 七、学习建议

### 1. 先做 NumPy 版

这是从零实现模型的版本，学生可以更直观看到：

- 输入数据如何处理
- 前向传播如何计算
- 损失函数如何定义
- 梯度如何更新

### 2. 再做 Paddle 版

Paddle 版让学生感受框架优势：

- 代码更简洁
- 自动求导
- 训练逻辑更清晰
- 对比 NumPy 版更容易理解“框架为何能提高效率”

### 3. 观察实验现象

建议学生改变参数后自己观察：

- loss 曲线是否更平滑
- 预测值是否更接近真实值
- 模型是否更稳定

---

## 八、项目结构

```text
ML_Housing-Price-Prediction/
├── README.md
├── main.ipynb
├── work/
│   ├── 1-2-build_neural_network_using_numpy.py
│   ├── 1-3-build_neural_network_using_paddle.py
│   ├── housing.data
│   └── housing.csv
├── generated_figures/
│   ├── loss_curve.png
│   ├── prediction_vs_actual.png
│   └── weight_distribution.png
├── LR_model.pdparams
└── .venv/
```

---

## 九、课堂使用建议

本项目非常适合教学环节：

- 第一节课：讲解数据处理与归一化
- 第二节课：讲解 NumPy 版训练过程
- 第三节课：讲解 Paddle 版框架实现
- 第四节课：对比两种版本并查看可视化结果

通过对比学习，学生能更直观地理解：

- 为什么深度学习框架能提高开发效率
- 为什么参数设置会影响模型效果
- 为什么可视化是模型分析的重要工具

---

## 十、总结

该项目既适合基础教学，也适合课堂演示。学生不需要复杂配置，只要修改少量参数并运行脚本，即可完成房价预测任务，并得到可视化输出结果。

如果想进一步提升模型效果，可以继续尝试：

- 调整学习率
- 改变批量大小
- 增加训练轮数
- 设计更复杂的网络结构

本项目的目标不是只跑通代码，而是帮助学生理解“机器学习从数据到模型，再到可视化分析”的完整流程。
