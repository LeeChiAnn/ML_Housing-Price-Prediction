# ML_Housing-Price-Prediction

> 基于波士顿房价数据集的机器学习房价预测教学项目
> 本项目为邯郸职业技术学院大数据技术专业综合实训项目，为机器学习入门项目
> 本项目基于百度AIStudio项目更改，欢迎提出问题与改进

## 简介

本项目使用经典的 **波士顿房价数据集（Boston Housing Dataset）** 进行房价预测，提供了两种神经网络实现方式，便于对比学习「底层原理」与「框架工程实践」：

- `1-2-build_neural_network_using_numpy.py`：用 **NumPy 从零实现** 神经网络
- `1-4-build_neural_network_using_paddle.py`：用 **PaddlePaddle** 框架实现神经网络

## 数据集

| 项目 | 说明 |
| --- | --- |
| 文件 | `housing.data` |
| 样本数 | 506 |
| 特征数 | 13（CRIM, ZN, INDUS, CHAS, NOX, RM, AGE, DIS, RAD, TAX, PTRATIO, B, LSTAT） |
| 目标变量 | `MEDV`（房价中位数，单位：千美元） |
| 格式 | 空格分隔的纯文本，无表头 |

## 环境要求

- Python 3.7+
- numpy
- paddlepaddle

```bash
pip install numpy paddlepaddle
```

## 目录结构

```
ML_Housing-Price-Prediction/
├── housing.data                              # 数据集
├── LR_model.pdparams                        # 模型权重
├── 1-2-build_neural_network_using_numpy.py  # NumPy 从零实现神经网络
├── 1-4-build_neural_network_using_paddle.py # PaddlePaddle 实现神经网络
├── 10663566.ipynb                           # AI Studio 项目 Notebook
└── README.md
```

> 若你的实际目录结构不同，请按本地文件调整本段。

## 运行

```bash
# 克隆仓库
git clone https://github.com/LeeChiAnn/ML_Housing-Price-Prediction.git
cd ML_Housing-Price-Prediction

# 安装依赖
pip install numpy paddlepaddle

# 运行示例
python 1-2-build_neural_network_using_numpy.py
python 1-4-build_neural_network_using_paddle.py
```

也可以直接在 Jupyter / AI Studio 中打开 `10663566.ipynb` 分步运行。

## 参考

- 波士顿房价数据集（UCI / StatLib）
- 飞桨 AI Studio 原项目

## 许可证

供教学与非商业用途使用。
