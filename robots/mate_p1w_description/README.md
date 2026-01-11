# Mate P1W Robot Description

Mate P1Wは**AGIRobots株式会社**による移動型セミヒューマノイドロボットです。  
本パッケージは、ロボットの **URDF モデル、メッシュファイル、および RViz2 による可視化ツール** を提供します。

本リポジトリは、主に **研究・開発（R&D）および可視化用途** を目的としています。

---

## 概要

このパッケージには以下が含まれます：

- URDF モデル  
- 可視化用メッシュファイル  
- Launch ファイル（RViz 自動起動スクリプト）  
- RViz 設定ファイル（プリセット済み）

---

## 想定ユーザー

- ROS 2 を使用したロボット研究・開発者  
- ロボットの構造や可動域を RViz 上で確認したい方  
- mate_p1w をベースに、制御・シミュレーション開発を行う開発者  

---

## インストール

```bash
cd ~/ros2_ws
colcon build --packages-select mate_p1w_description
source install/setup.bash
```

---

## 使用方法

```bash
ros2 launch mate_p1w_description display.launch.py
```

- RViz2：3D モデル表示  

<img width="1552" height="814" alt="mate_p1w_display launch py" src="https://github.com/user-attachments/assets/5a17fd72-6448-47b6-b21e-32066d7ada01" />

- Joint State Publisher GUI：関節角度操作

<img width="1552" height="822" alt="mate_p1w_display launch py jointstatepublisher" src="https://github.com/user-attachments/assets/1aed9821-61c1-4520-ba94-c8eb299fc31e" />

---

## ディレクトリ構成

```
mate_p1w_description/
├── urdf/
├── meshes/
├── launch/
└── rviz/
```

---

## 制限事項

- 本パッケージは可視化・構造確認用です  
- 実機制御・走行制御は含まれません  

---

## 本パッケージの位置づけ

本リポジトリは **製品ではありません**。  
AGIRobots では、別途 **製品リリースを前提としたロボット開発** を進めています。

---

## Feedback / Contact

技術的な質問、研究・PoC 利用、将来的な協業に関するご相談があればご連絡ください。

---

## Citation

```bibtex
@misc{agirobots_mate_p1w_description,
  title        = {AGIRobots ROS},
  author       = {{AGIRobots Inc.}},
  year         = {2026},
  howpublished = {https://github.com/AGIRobots/agirobots_ros}
}
```

---

## License

Copyright (c) AGIRobots Inc.
