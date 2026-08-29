# Civil GUI Enhancement and Update

## 📋 项目简介

本项目是橡胶混凝土（Rubber Concrete）力学性能预测研究的 GUI 应用程序迭代开发仓库。通过集成 6 种机器学习模型与 9 个输入特征，实现混凝土配合比的智能化设计与性能预测。

## 📁 项目结构

```
Civil-GUI-Enhancement-and-Update/
├── 6 模型 9 输入 1 输出/
│   └── 5.基于新控制变量法下的最大粒径区间对比/
│       ├── T3RC_V40_1.m              # 主控制程序
│       ├── T3_LSBoost.m              # LSBoost 模型脚本
│       ├── ConcreteModel_LSBoost.mat # 训练好的 LSBoost 模型
│       ├── 数据集 3.xlsx               # 实验数据集
│       └── p1-p8 系列.xlsx            # 控制变量法参数文件
│
└── 论文代码/
    ├── 数据集/
    │   ├── Database of rubberized concrete and its compressive strength.xlsx
    │   ├── 数据集 2-5.xlsx
    │   └── 数据说明
    │
    └── 输入输出/
        ├── 6 模型 8 输入 1 输出/       # 8 特征版本（6 种模型）
        │   ├── 1.PSO-SVR 完善（1）
        │   ├── 2.RF 完善（2-10）
        │   ├── 3.XG-Boost 完善（4-42）
        │   ├── 4.GA-BP 神经网络完善（4-7）
        │   ├── 5.LSSVM 完善（4-36）
        │   └── 6.LSTM 完善深度学习（4-21）
        │
        └── 6 模型 9 输入 1 输出/       # 9 特征版本
            ├── 1.模型整合/            # 6 种模型集成 + GA 优化 + LSSVM 工具箱
            ├── 2.消融实验/            # 消融实验分析与结果图
            ├── 3.泛化盲测验证实验/     # 盲测验证 + GUI 输出结果
            └── 4.GUI/                 # GUI 应用程序及输出
```

## 🤖 机器学习模型

项目实现并对比了 **6 种** 机器学习模型：

| 模型 | 优化算法 | 说明 |
|:-----|:---------|:-----|
| PSO-SVR | 粒子群优化 | 支持向量回归 |
| RF | - | 随机森林 |
| XGBoost (LSBoost) | PSO | 提升树集成 |
| GA-BP | 遗传算法 | 反向传播神经网络 |
| LSSVM | PSO | 最小二乘支持向量机 |
| LSTM | - | 长短期记忆网络 |

## 📊 数据集

- **输入特征**：8 或 9 个混凝土配合比参数（水泥用量、水胶比、橡胶掺量、粒径等）
- **输出目标**：抗压强度（1 个）
- **数据集版本**：数据集 2、3、4、5（ progressively refined）

## 🔬 研究内容

### 1. 模型整合（9 输入 1 输出）
- 6 种机器学习模型的统一框架
- GA 优化算法工具箱（goat 文件夹）
- LSSVM 工具箱集成

### 2. 消融实验
- 8 输入 vs 9 输入特征对比
- PSO-LSBoost 单模型分析
- 性能评估指标：R²、RMSE、MAE

### 3. 泛化盲测验证
- 独立测试集验证
- GUI 批量预测与盲审对比
- SHAP 特征重要性分析
- 科学图表自动生成（.fig 格式）

### 4. GUI 应用程序
- 智能设计系统（T3RC_V38/V39）
- 批量预测功能
- 盲测审核功能
- 设计日志自动记录

## 🚀 使用说明

### 环境要求
- MATLAB R2020b 或更高版本
- Statistics and Machine Learning Toolbox
- Deep Learning Toolbox（LSTM 模型）
- LSSVM 工具箱（已包含在 `1.模型整合/LSSVM_Toolbox`）

### 运行模型

```matlab
% 运行 LSBoost 模型
cd('6 模型 9 输入 1 输出/5.基于新控制变量法下的最大粒径区间对比')
run('T3_LSBoost.m')

% 运行 6 模型整合
cd('论文代码/输入输出/6 模型 9 输入 1 输出/1.模型整合')
run('T7_Main.m')

% 运行消融实验
cd('论文代码/输入输出/6 模型 9 输入 1 输出/2.消融实验')
run('main.m')
```

### GUI 使用
```matlab
cd('论文代码/输入输出/6 模型 9 输入 1 输出/4.GUI')
% 运行 GUI 主程序（具体文件名待确认）
```

## 📈 输出成果

- **预测结果**：Excel 格式（Batch_Result_*.xlsx, Design_Log_*.xlsx）
- **科学图表**：MATLAB .fig 格式 + PNG 导出
- **模型文件**：.mat 格式（ConcreteModel_LSBoost.mat 等）
- **消融实验报告**：Final_Ablation_Analysis_Report.png

## 📝 版本迭代

| 版本 | 输入特征 | 输出 | 说明 |
|:-----|:--------|:-----|:-----|
| V1-V3 | 8 | 1 | 基础模型开发 |
| V37-V39 | 9 | 1 | 添加粒径特征，GUI 迭代 |
| V40 | 9 | 1 | 控制变量法分析 |

## 👨‍💻 作者

- **Li Ding** (李鼎)
- GitHub: [@Li-Ding-PhDL](https://github.com/Li-Ding-PhDL)

## 📄 许可证

MIT License

---

**最后更新**: 2026 年 8 月 29 日
