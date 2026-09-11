# Public Tank Detection YOLO Model

# 公开坦克目标检测 YOLO 模型

## Model summary / 模型摘要

| Item / 项目 | Value / 数值 |
| --- | ---: |
| Model family / 模型系列 | YOLO11n fine-tuned for one class |
| Class / 类别 | `tank` |
| Training preset / 训练档位 | High |
| Epochs / 训练轮数 | 100 |
| Input size / 输入尺寸 | 960 × 960 |
| Batch / 批大小 | 4 |
| Data-loader workers / 数据线程 | 1 |
| Device / 设备 | AMD Radeon RX 9070 XT, 16GB |
| Backend / 后端 | ROCm/HIP, single GPU |
| Run status / 运行状态 | Complete / 已完成 |

## Test result / 测试结果

Evaluation was performed on the held-out test split of the merged dataset. The test split contains 157 images and 590 annotated boxes, including 40 negative images.

评估使用合并数据集的独立 test split，共 157 张图片、590 个标注框，其中包含 40 张负样本图片。

| Metric / 指标 | Result / 结果 |
| --- | ---: |
| Precision | 0.8069 |
| Recall | 0.6871 |
| mAP@0.5 | 0.7544 |
| mAP@0.5:0.95 | 0.4231 |
| Mean inference time / 平均推理时间 | 78.1 ms/image |

These are research-baseline results, not a guarantee of generalization or deployment readiness. Recall and strict localization remain limited; users should test on their own authorized data before drawing conclusions.

这些是研究基线结果，不代表泛化能力或可部署性。当前召回率和严格定位能力仍有限，使用者应在自有且获授权的数据上继续验证。

## Dataset composition / 数据集组成

The merged dataset was normalized to one class, `tank`. Original source material and full annotations are intentionally not redistributed here.

合并数据集统一为单一类别 `tank`。原始素材和完整标注不会在此仓库重新分发。

| Source label / 来源 | Images / 图片 | Train | Val | Test | Boxes / 框 | Local review / 本地审查 |
| --- | ---: | ---: | ---: | ---: | ---: | --- |
| Simuletic UAV Tank | 164 | 131 | 16 | 17 | 716 | License copy not present locally |
| MCA Tanks | 1,235 | 1,074 | 120 | 41 | 18,700 | Download record says Public Domain; verify source page |
| Military Vehicle Detection, tank subset | 1,130 | 880 | 151 | 99 | 1,973 | Download record says MIT; verify source page |
| **Merged total** | **2,529** | **2,085** | **287** | **157** | **21,389** | |

Source links and the exact version/permission review are listed in [DATASET_NOTICES.md](DATASET_NOTICES.md).

