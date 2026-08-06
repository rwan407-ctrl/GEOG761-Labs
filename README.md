# GEOG 761 — Satellite Data and AI (2026 S2) · my working copies

我在这门课的 lab / 课堂练习工作副本。上游是老师的官方仓库
[tpfd/SatelliteDataAI-UOA](https://github.com/tpfd/SatelliteDataAI-UOA)（commit `2cfd300`, 2026-07-31）。

**在 Colab 里打开就能改、能存**（改完 `File → Save a copy in GitHub` 提交回本仓库）：

| | Colab |
|---|---|
| Lab 1 卫星数据入门 | [761_Lab1.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lab1.ipynb) |
| Lab 2 土地覆盖分类 | [761_Lab2.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lab2.ipynb) |
| Lab 3 进阶去云 | [761_Lab3.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lab3.ipynb) |
| Lab 4 CNN 找太阳能板 | [761_Lab4.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lab4.ipynb) |
| Lab 5 语义分割 | [761_Lab5.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lab5.ipynb) |
| 练习 L2 随机森林 | [761_Lecture2_Exercises.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lecture2_Exercises.ipynb) |
| 练习 L3 K-means | [761_Lecture3_Exercsies.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lecture3_Exercsies.ipynb) |
| 练习 L5 CNN 入门 | [761_Lecture5_Exercises.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lecture5_Exercises.ipynb) |
| 练习 L8 SAR 雷达 | [761_Lecture8_Exercises.ipynb](https://colab.research.google.com/github/rwan407-ctrl/GEOG761-Labs/blob/main/761_Lecture8_Exercises.ipynb) |

## 相对官方版改了什么

1. `ee.Initialize(project=...)` 从老师的 `earthengine-ml-testing` 换成 **`geog761-ai`**
   （我自己的 GEE 项目，在 wangruofan126@gmail.com 名下，已注册非商业用途 / 社区层级）。
   Lab4 和 Lecture2 练习不用 Earth Engine，没有这一行。
2. 清掉了 cell 的运行输出，方便看 diff。

## 用之前要知道的

- Colab 打开时账号必须是 **wangruofan126@gmail.com**，因为 `geog761-ai` 在这个号下。
- Lab 4 / Lab 5 要 GPU：代码执行程序 → 更改运行时类型 → GPU。
- Lab 4 的训练数据 `train.zip`（79 MB）不在仓库里，从 Canvas → Files 或
  [Solafune](https://solafune.com/competitions/5dfc315c-1b24-4573-804f-7de8d707cd90) 拿。

## 跟上游同步

老师本学期一直在改官方仓库，做新 lab 之前先看看有没有更新：

```bash
git remote add upstream https://github.com/tpfd/SatelliteDataAI-UOA.git   # 只需一次
git fetch upstream && git log --oneline HEAD..upstream/main
```
