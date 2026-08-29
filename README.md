# Civil GUI Enhancement and Update

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?logo=windows)](https://www.microsoft.com/windows)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## 📋 项目简介

本项目是一个面向土木工程材料研究的 **图形用户界面 (GUI) 应用程序**，旨在为混凝土力学性能研究提供便捷、高效的可视化工具。通过不断迭代优化 GUI 功能，简化橡胶混凝土等新型建筑材料的实验数据分析流程。

## 🔬 研究背景

在混凝土材料研究中，实验数据的处理、分析和可视化往往需要大量的手动操作和重复性工作。本项目通过开发专用的 GUI 应用程序，实现：
- 实验数据的快速导入与预处理
- 力学性能的可视化对比分析
- 控制变量法下的参数敏感性分析
- 研究结果的自动化报告生成

## 📁 文件结构

```
Civil-GUI-Enhancement-and-Update/
├── 5.基于新控制变量法下的最大粒径区间对比/   # 控制变量法分析模块
│   └── [相关分析脚本与数据文件]
├── 论文代码/                                  # 学术论文配套代码
│   └── [论文中使用的核心算法与 GUI 源码]
└── README.md                                  # 项目说明文档
```

## 🎯 核心功能

### 1. 数据管理与预处理
- ✅ Excel/CSV 数据文件批量导入
- ✅ 数据清洗与异常值检测
- ✅ 自动归一化与标准化处理
- ✅ 训练集/测试集智能划分

### 2. 力学性能分析
- ✅ 抗压强度预测与对比
- ✅ 抗折强度分析
- ✅ 弹性模量计算
- ✅ 应力 - 应变曲线可视化

### 3. 控制变量法分析
- ✅ 单因素敏感性分析
- ✅ 多因素交互作用可视化
- ✅ 最大粒径区间对比分析
- ✅ 参数优化建议生成

### 4. 可视化输出
- ✅ 多维度数据对比图表
- ✅ 预测值 vs 实际值散点图
- ✅ 误差分布直方图
- ✅ 等高线图与热力图
- ✅ 可导出高清图片 (PNG/SVG)

## 💻 技术栈

| 类别 | 技术 |
|:----:|:-----|
| **开发语言** | MATLAB / Python (待确认) |
| **GUI 框架** | MATLAB App Designer / PyQt / Tkinter |
| **数据处理** | Pandas / MATLAB Table |
| **可视化** | Matplotlib / MATLAB Plotting |
| **数据格式** | Excel (.xlsx), CSV, MAT |

## 🚀 快速开始

### 环境要求
- Windows 10/11 操作系统
- MATLAB R2020b+ 或 Python 3.8+
- 相关工具箱（如使用 MATLAB）：
  - Statistics and Machine Learning Toolbox
  - Curve Fitting Toolbox

### 安装步骤

1. **克隆仓库**
   ```bash
   git clone https://github.com/Li-Ding-PhDL/Civil-GUI-Enhancement-and-Update.git
   cd Civil-GUI-Enhancement-and-Update
   ```

2. **安装依赖**（如使用 Python）
   ```bash
   pip install -r requirements.txt
   ```

3. **运行 GUI 程序**
   ```matlab
   % MATLAB 版本
   run('main_gui.m')
   
   # 或 Python 版本
   python main_gui.py
   ```

### 使用说明

1. **数据导入**：点击"导入数据"按钮，选择 Excel/CSV 文件
2. **参数设置**：在设置面板中选择分析类型和参数
3. **运行分析**：点击"开始分析"按钮执行计算
4. **查看结果**：在结果面板查看图表和数据
5. **导出报告**：点击"导出报告"保存分析结果

## 📊 典型应用场景

| 场景 | 功能模块 | 输出 |
|:-----|:--------|:-----|
| 橡胶混凝土配合比优化 | 控制变量法分析 | 最优掺量建议 |
| 力学性能预测 | 回归分析模块 | R²、RMSE 指标 |
| 粒径效应研究 | 最大粒径区间对比 | 对比柱状图 |
| 论文数据可视化 | 图表导出模块 | 高清 publication-ready 图片 |

## 📝 更新日志

### v1.0 (2026)
- 初始版本发布
- 基础数据导入功能
- 控制变量法分析模块
- 基础可视化功能

### 待更新
- [ ] 多语言支持（中文/英文）
- [ ] 批量数据处理
- [ ] 机器学习模型集成
- [ ] 报告自动生成

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)

## 👨‍💻 作者信息

- **Li Ding** (李鼎)
- GitHub: [@Li-Ding-PhDL](https://github.com/Li-Ding-PhDL)

## 🤝 贡献指南

欢迎通过以下方式参与项目：
1. 提交 Issue 报告问题或提出功能建议
2. Fork 仓库并提交 Pull Request
3. 分享您的使用经验和改进方案

## 📧 联系方式

如有学术合作或技术咨询需求，请通过以下方式联系：
- GitHub Issues
- Email: (待添加)

## 🙏 致谢

感谢所有为本项目提供反馈和建议的研究人员！

---

**最后更新**: 2026 年 8 月 29 日
