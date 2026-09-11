# Weight notice / 权重声明

The file `weights/best.pt` is a privacy-sanitized YOLO checkpoint trained from three public-source datasets. The source dataset files, annotations, and training logs are not included.

`weights/best.pt` 是一个已经清理本机路径等隐私信息的 YOLO 检查点，使用三个公开来源数据集训练。仓库不包含原始数据集文件、标注和训练日志。

## Scope / 使用范围

- Non-commercial research, education, and personal learning only.
- Do not use for harmful, unlawful, privacy-invasive, safety-critical, or regulated decisions.
- Do not infer that the weight is suitable for deployment or operational decisions.

- 仅限非商业研究、教育和个人学习。
- 不得用于有害、违法、侵犯隐私、安全关键或受监管的决策。
- 不应据此推断该权重适合部署或运行任务决策。

## Source and attribution / 来源与署名

The contributor confirms that the local Simuletic copy used for training was the approximately 140 MB free sample portion. The public source describes its sample as available under CC BY 4.0; users should retain attribution to Simuletic and verify the terms for any different source version.

贡献者确认，训练使用的是约 140 MB 的 Simuletic 免费样本部分。公开来源将其样本描述为 CC BY 4.0；使用其他来源版本时，应重新核对条款，并保留对 Simuletic 的署名。

- [Simuletic dataset card](https://huggingface.co/datasets/Simuletic/UAV-Aerial-View-Battle-Tank-Detection-Dataset)
- [Simuletic sample information](https://simuletic.com/blog/uav-battle-tank-dataset)
- [MCA Project Tanks source](https://universe.roboflow.com/mca-project/tanks-upqfi/dataset/3)
- [Military Vehicle Detection source](https://universe.roboflow.com/tracking-baj9f/military-vehicle-detection-juleg-4mmde/dataset/1)

## Integrity / 完整性

- File: `weights/best.pt`
- SHA-256: `81DD8A702F5AAE323B5712A182A8F650B26CEBD778527CABE39EB0AB203564A2`
- Size: 5,544,026 bytes

The checkpoint was loaded successfully after privacy sanitization; embedded local paths were removed before publication.

隐私清理后已成功加载检查点；发布前已移除其中嵌入的本机路径。
