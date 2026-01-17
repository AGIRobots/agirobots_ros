# agirobots_ros

AGIRobots が開発するロボットプラットフォーム向けの ROS 2 パッケージ群（主に Description / 可視化用途）をまとめた公式リポジトリです。

本リポジトリは研究・開発（R&D）用途を主目的とし、ロボットモデルの可視化、シミュレーション連携、将来的な制御拡張のためのベースを提供します。

---

## 概要（Overview）

agirobots_ros は、AGIRobots が開発する複数のロボットハードウェアに対して、ROS 2 ベースでの開発・評価を行うためのリポジトリです。

現時点では、以下を主な対象としています。

* ロボット記述（URDF / Xacro）
* RViz による可視化
* ROS 2 ワークスペース構成の提供
* 将来的な制御・シミュレーション拡張のための土台

---

## 対応ロボット（Supported Robots）

### Mate P1W

* 移動型セミヒューマノイド（車輪移動ベース＋上半身）
* 研究・開発向けプラットフォーム
* 主に URDF / RViz による可視化用途を想定

パッケージ：`robots/mate_p1w_description`

### SB1 Core

* スワーブ駆動型 移動ロボットベース
* 上位ロボットや派生機のためのコアプラットフォーム
* 構造・可動域確認を目的とした Description

パッケージ：`robots/sb1_core_description`

---

## 動作環境（Environment）

* ROS 2 Humble（推奨）
* ROS 2 Jazzy（検証中）

---

## インストール（Installation）

本リポジトリは、ROS 2 ワークスペースの `src/` 配下に配置してビルドします。

```bash
mkdir -p ~/agirobots_ws/src
cd ~/agirobots_ws/src
git clone https://github.com/AGIRobots/agirobots_ros.git
cd ..
colcon build
source install/setup.bash
```

### Description パッケージのみビルドする場合

```bash
cd ~/agirobots_ws
colcon build --packages-select mate_p1w_description sb1_core_description
source install/setup.bash
```

---

## クイックスタート（Quick Start）

### Mate P1W を RViz で表示

```bash
ros2 launch mate_p1w_description mate_p1w_display.launch.py
```

### SB1 Core を RViz で表示

```bash
ros2 launch sb1_core_description sb1_core_display.launch.py
```

---

## リポジトリ構成（Repository Structure）

```text
agirobots_ros/
├── robots/
│   ├── mate_p1w_description/
│   │   ├── urdf/
│   │   ├── meshes/
│   │   ├── launch/
│   │   └── rviz/
│   └── sb1_core_description/
│       ├── urdf/
│       ├── meshes/
│       ├── launch/
│       └── rviz/
└── README.md
```

---

## 注意事項（Notes）

* 本リポジトリは研究・開発用途を主目的としています
* 実機向けの低レベル制御、ドライバ、走行制御は含まれていません
* API やディレクトリ構成は今後変更される可能性があります

---

## Citation

```bibtex
@misc{agirobots_ros,
  title        = {AGIRobots ROS},
  author       = {{AGIRobots Inc.}},
  year         = {2026},
  howpublished = {https://github.com/AGIRobots/agirobots_ros}
}
```

---

## License

TBD
