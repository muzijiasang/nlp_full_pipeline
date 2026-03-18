# 📁 项目结构
NLP_FULL_PIPELINE/

├── notebooks/                  # 核心代码与实验脚本

│   ├── data_preparation.ipynb      # 数据清洗、预处理与格式转换

│   ├── text_classification.ipynb   # 文本分类模型训练与推理

│   ├── information_extraction.ipynb # 命名实体识别（NER）等信息抽取任务

│   └── evaluation_analysis.ipynb   # 模型结果可视化与指标分析

├── data/

│   ├── raw/                      # 原始未处理数据

│   └── processed/                # 清洗后可直接用于训练的数据集

├── models/

│   ├── text_classification/      # 保存训练好的文本分类模型

│   └── ner/                      # 保存训练好的NER模型

├── reports/                      # 实验结果与可视化报告

│   ├── confusion_matrix.png          # 分类任务混淆矩阵

│   ├── text_classification_cm.png    # 文本分类混淆矩阵

│   ├── ner_metrics.png               # NER任务性能指标图

│   ├── overall_metrics.png            # 整体模型性能汇总图

│   ├── text_classification_results.json # 文本分类结果JSON

│   ├── ner_results.json               # NER结果JSON

│   └── training_results.json         # 训练过程指标记录

└── requirements.txt             # 项目依赖环境
***
# ✨ 项目功能
Track A：文本分类

支持情感分析、垃圾邮件检测、意图识别等多类别文本分类任务，提供完整的模型训练、验证与推理流程，自动生成混淆矩阵、准确率 / 精确率 / 召回率 / F1 等评估指标

Track B：信息抽取

聚焦命名实体识别（NER），可扩展至关系抽取、关键短语提取，支持实体边界与类型标注、批量文本抽取，生成精确率、召回率、F1 等 NER 专项评估指标
# 🚀 快速开始
1. 环境准备
   
**bash**

运行

**pip install -r requirements.txt**

3. 数据准备
将原始数据放入 data/raw/ 目录

运行 notebooks/data_preparation.ipynb 完成数据清洗、分词、格式转换

处理后的数据将自动保存至 data/processed/

4. 模型训练

文本分类：运行 notebooks/text_classification.ipynb

信息抽取（NER）：运行 notebooks/information_extraction.ipynb

训练完成的模型将保存至 models/ 对应目录
5. 结果评估与分析

运行 notebooks/evaluation_analysis.ipynb：

加载模型预测结果

生成混淆矩阵、性能曲线等可视化图表（保存至 reports/）

输出结构化 JSON 结果，便于后续分析与报告撰写
# 📊 输出结果
reports/*.png	模型性能可视化图表（混淆矩阵、指标曲线等）

reports/*.json	结构化结果数据（分类 / NER 结果、训练日志）

models/	训练好的模型权重与配置文件
# 🛠️ 技术栈
Python 3.8+
核心库：scikit-learn, transformers, torch, pandas, numpy
可视化：matplotlib, seaborn
开发环境：Jupyter Notebook
# 📝 注意事项
请确保 data/processed/ 目录下的数据集格式与模型输入要求一致

训练前可根据硬件资源调整 notebooks 中的 batch size、epoch 等超参数

评估脚本依赖训练阶段生成的结果文件，请确保先完成模型训练
# 🤝 贡献
欢迎提交 Issue 与 Pull Request 来完善项目。

[link](https://github.com/muzijiasang/nlp_full_pipeline)
