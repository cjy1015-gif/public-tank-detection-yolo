# Reproduction notes / 复现说明

This preview intentionally does not contain the datasets or model weights. Reproduction requires obtaining the exact source versions through their official pages and using only data whose terms permit your intended use.

本预览刻意不包含数据集和模型权重。复现时必须从官方页面获取精确来源版本，并且只能使用许可条款允许你目标用途的数据。

## Environment / 环境

- Windows 11 + WSL2 Ubuntu 24.04
- AMD Radeon RX 9070 XT, 16GB VRAM
- 16GB host memory
- ROCm/HIP PyTorch environment
- Single GPU

## Data preparation / 数据准备

1. Keep each source dataset in a separate private directory.
2. Record the source URL, version, license text, and archive hash.
3. Normalize the selected class to `tank`.
4. Keep train/validation/test source groups separate where the source metadata supports it.
5. Quarantine duplicates instead of silently overwriting them.
6. Generate a private manifest and SHA-256 fingerprint.
7. Run a format precheck before training.

1. 将每个来源数据集放在独立的私有目录。
2. 记录来源网址、版本、许可证文本和归档哈希。
3. 将目标类别统一为 `tank`。
4. 在来源元数据允许时保持 train/validation/test 来源组隔离。
5. 对重复文件隔离保存，不要静默覆盖。
6. 生成私有清单和 SHA-256 指纹。
7. 训练前执行格式预检。

## Training / 训练

Use the values in [`yolo-public-merged.example.yaml`](../configs/yolo-public-merged.example.yaml) as a starting point. Keep output directories, logs, manifests, and weights outside the public repository.

以 [`yolo-public-merged.example.yaml`](../configs/yolo-public-merged.example.yaml) 中的参数作为起点。输出目录、日志、清单和权重都应放在公开仓库之外。

## Validation / 验证

- Confirm the run exits normally.
- Confirm `best.pt` and `last.pt` are both written privately.
- Confirm the test split is fixed before comparing runs.
- Record Precision, Recall, mAP@0.5, mAP@0.5:0.95, and inference timing.
- Inspect false positives and false negatives, not only the aggregate scores.
- Do not upload the weight until the dataset notice release gate is complete.

- 确认训练正常退出。
- 私下确认 `best.pt` 和 `last.pt` 均已写出。
- 比较不同训练时固定测试集不变。
- 记录 Precision、Recall、mAP@0.5、mAP@0.5:0.95 和推理时间。
- 不只看汇总指标，还要检查误报和漏检。
- 数据集声明审查完成前，不上传权重。
