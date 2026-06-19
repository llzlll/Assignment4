# 3DGS (3D Gaussian Splatting) 重建项目

基于3D Gaussian Splatting技术的场景三维重建实现。

## 项目结构

```
04_3DGS/
├── data/              # 数据集
├── vedio/             # 结果视频
├── data_utils.py      # 数据处理工具
├── gaussian_model.py  # 高斯模型定义
├── gaussian_renderer.py # 高斯渲染器
├── train.py           # 训练脚本
├── render_3dgs_mv.py  # 渲染脚本
└── README.md          # 项目说明
```

## 结果展示

### Task 2: 多视图渲染结果

<div align="center">
  <video src="vedio/render_mv.mp4" width="600" controls></video>
</div>

### Task 3: 3DGS 重建结果

<div align="center">
  <video src="vedio/3DGS重建结果.mp4" width="600" controls></video>
</div>

## 结果说明

Task 3 的椅子底部重建结果较模糊，这是由于缺少底部视角的数据导致的。在3D Gaussian Splatting重建中，多视角的覆盖完整性直接影响重建质量，底部视角的缺失使得该区域的几何细节无法准确恢复。

## 依赖

- PyTorch
- PyTorch3D
- COLMAP

## 使用方法

```bash
# 训练
python train.py

# 渲染
python render_3dgs_mv.py
```