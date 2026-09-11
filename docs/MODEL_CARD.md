# Model card / 模型卡片

## Intended use / 预期用途

This is a single-class object detector for research on visual tank detection. It is intended for offline evaluation, reproducibility exercises, and comparison of training choices.

这是一个用于视觉坦克目标检测研究的单类别目标检测器，适合离线评估、复现实验和训练方案对比。

It is not presented as a reliable detector for operational, safety-critical, surveillance, targeting, or regulated decisions.

它不被宣称适合运行任务、安全关键、监控、目标决策或受监管场景。

## Training recipe / 训练方案

- Base: YOLO11n checkpoint already available in the local project
- One class: `tank`
- Three normalized public-source datasets
- 100 epochs
- Input size: 960
- Batch size: 4
- Workers: 1
- Single AMD GPU through ROCm/HIP
- Test metric confidence: 0.001
- Sample visualization confidence: 0.25

- 基础模型：本地项目已有的 YOLO11n 检查点
- 单类别：`tank`
- 三个公开来源数据集，经统一清洗和类别归一化
- 100 轮训练
- 输入尺寸：960
- batch size：4
- 数据线程：1
- 通过 ROCm/HIP 使用单张 AMD 显卡
- 测试指标置信度：0.001
- 样例图显示置信度：0.25

## Evaluation / 评估

| Metric / 指标 | Value / 数值 |
| --- | ---: |
| Test images / 测试图片 | 157 |
| Test boxes / 测试框 | 590 |
| Precision | 0.8069 |
| Recall | 0.6871 |
| mAP@0.5 | 0.7544 |
| mAP@0.5:0.95 | 0.4231 |
| Mean inference / 平均推理 | 78.1 ms/image |

The held-out split is relatively small and source-domain composition can affect the score. Reported metrics should not be compared with another run unless class definitions, split policy, image size, confidence protocol, and test data are aligned.

独立测试集规模有限，来源构成会影响分数。除非类别定义、数据划分、输入尺寸、置信度协议和测试数据完全一致，否则不应将这些指标与其他训练运行直接比较。

## Limitations / 局限

- A single `tank` class does not distinguish vehicle types or friendly/hostile status.
- Source-domain differences may cause false positives or missed detections.
- The test split was checked for format errors, but complete source-clip separation was not independently recorded in the public package.
- No claim is made about real-time performance on other hardware.
- The released weight is limited to non-commercial research and learning under the source-attribution notice.

- 单一 `tank` 类别不区分车型，也不判断敌我属性。
- 数据来源差异可能导致误报或漏检。
- 测试集通过格式预检，但公开包没有独立记录完整来源片段隔离证据。
- 不对其他硬件上的实时性能作保证。
- 发布权重仅限非商业研究和学习用途，并受来源署名声明约束。
