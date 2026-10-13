# lztyolo

YOLOv9 目标检测实验工作区。

> 代码位于 [`yolov9/`](yolov9/) 子目录，基于 YOLOv9 官方实现。

## 目录结构

```
yolov9/
├── train.py / train_dual.py / train_triple.py     训练（单分支 / dual / triple）
├── val.py   / val_dual.py   / val_triple.py       验证
├── detect.py / detect_dual.py                     推理
├── segment/      分割任务（train / val / predict）
├── panoptic/     全景分割任务
├── classify/     分类任务
├── models/       模型结构与配置
│   └── detect/   gelan-*.yaml、yolov9-*.yaml、yolov7-af.yaml ...
├── utils/        数据加载、损失（loss_tal / loss_tal_dual / loss_tal_triple）、指标、日志等
├── tools/        重参数化笔记本（reparameterization.ipynb）
├── requirements.txt
└── yolov9-c.pt   预训练权重
```

## 环境

```bash
cd yolov9
pip install -r requirements.txt
```

## 使用

```bash
# 训练、验证、推理（具体参数以各脚本的 --help 为准）
python train_dual.py
python val_dual.py
python detect_dual.py
```

> 数据集与训练输出不在本仓库内，需自行准备并在脚本中配置。

---

> 本 README 依据仓库现有代码整理，细节如与实现不符请以代码为准。
