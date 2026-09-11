# Dataset notices / 数据集声明

This file records the release review status. A dataset being publicly downloadable does not automatically mean that a derived model may be redistributed without attribution or additional restrictions.

本文记录发布审查状态。数据集可以公开下载，并不自动意味着基于它训练的模型可以不署名、无条件重新分发。

## Source review / 来源审查

### 1. Simuletic UAV Tank

- Local training copy: 164 images after normalization.
- The contributor confirms that the local copy used here was the approximately 140 MB free sample portion.
- The release is limited to non-commercial research and learning, with attribution to Simuletic.
- A public dataset card currently displays `cc-by-nc-4.0`, while a separate public page describes the free sample under CC BY 4.0. Users must recheck the terms when using a different source version.

- 本地训练副本：统一处理后 164 张图片。
- 贡献者确认，本次使用的本地副本是约 140 MB 的免费样本部分。
- 本次发布限定为非商业研究和学习，并保留对 Simuletic 的署名。
- 当前公开的数据卡显示 `cc-by-nc-4.0`，另一个公开页面将免费样本描述为 CC BY 4.0。使用其他来源版本时必须重新核对条款。

Candidate source pages / 待核对来源：

- [Simuletic dataset card](https://huggingface.co/datasets/Simuletic/UAV-Aerial-View-Battle-Tank-Detection-Dataset)
- [Simuletic dataset information](https://simuletic.com/blog/uav-battle-tank-dataset)

### 2. MCA Tanks

- Local export metadata says `Public Domain`.
- The exact Roboflow Universe version should remain linked in attribution and be checked again immediately before release.

- 本地导出元数据标注为 `Public Domain`。
- 发布时应保留对应 Roboflow Universe 版本链接，并在正式发布前再次核对页面信息。

Source / 来源：[MCA Project Tanks dataset](https://universe.roboflow.com/mca-project/tanks-upqfi/dataset/3)

### 3. Military Vehicle Detection

- Local export metadata says `MIT`; only the tank subset was retained for this experiment.
- The upstream page, version, attribution, and any dataset-specific conditions should be preserved and rechecked before redistributing a derived weight.

- 本地导出元数据标注为 `MIT`；本实验只保留了其中的 tank 子集。
- 重新分发衍生权重前，应保留并再次核对上游页面、版本、署名和数据集特定条件。

Source / 来源：[Military Vehicle Detection dataset](https://universe.roboflow.com/tracking-baj9f/military-vehicle-detection-juleg-4mmde/dataset/1)

## Release gate / 发布门槛

Before adding a weight file to a public release:

1. Match each local dataset copy to an exact public version or archive hash.
2. Save the license text, attribution requirements, and access terms privately and in the repository notices.
3. Check whether the least permissive source limits commercial use, redistribution, or model derivatives.
4. Confirm that the base YOLO implementation and any pretrained checkpoint allow the intended redistribution.
5. For a different source version or commercial use, recheck the combined terms before use.

在把权重文件加入公开发布前：

1. 将每个本地数据副本对应到精确的公开版本或归档哈希。
2. 保存许可证文本、署名要求和访问条款，并写入仓库声明。
3. 检查限制最严格的来源是否限制商业使用、再分发或模型衍生品。
4. 确认 YOLO 基础实现和预训练检查点允许目标发布方式。
5. 如果使用其他来源版本或涉及商业用途，应在使用前重新核对组合条款。
