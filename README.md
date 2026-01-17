# agirobots_ros

AGIRobotsが開発するロボットプラットフォーム向けのROS2パッケージ群をまとめたリポジトリです。

本リポジトリは、研究・開発用途を主目的とし、ロボットモデルの可視化、シミュレーション連携、将来的な制御拡張のためのベースを提供します。

<img width="2398" height="1260" alt="mate_p1w_display launch py jointstatepublisher" src="https://github.com/user-attachments/assets/27dd934a-8aad-40a9-8a8f-c63c69be7d45" />

## 概要（Overview）

agirobots_rosは、AGIRobotsが提供するロボットハードウェアに対して、ROS2ベースでの開発・評価を行うための公式リポジトリです。

現時点では、以下を主な対象としています。

- ロボット記述（URDF / Xacro）

- RViz による可視化

- ROS2ワークスペース構成の提供

- 今後の制御・シミュレーション拡張のための土台

## 対応ロボット（Supported Robots）
### Mate P1W

- 車輪移動型ベース＋上半身ヒューマノイド構成

- 研究・開発向けプラットフォーム

- 主に可視化・モデル確認用途を想定

## 動作環境（Environment）

- ROS 2 Humble（推奨）

- ROS 2 Jazzy（検証中）

## インストール方法（Installation）
```bash
mkdir -p ~/agirobots_ws/src
cd ~/agirobots_ws/src
git clone https://github.com/AGIRobots/agirobots_ros.git
cd ..
colcon build
source install/setup.bash
```

## クイックスタート（Quick Start）

RVizでロボットモデルを表示する

```bash
ros2 launch mate_p1w_description display.launch.py
```

RViz が起動し、Mate P1W のロボットモデルが表示されます。

## パッケージ構成（Packages）

Mate P1W 用のロボット記述パッケージです。

主な内容：

- URDF / Xacro

- メッシュファイル

- RViz設定

- 可視化用 launch ファイル

## 注意事項（Notes）

- 本リポジトリは現在開発途中です

- APIやディレクトリ構成は今後変更される可能性があります

- 本リポジトリには、低レベルのモータ制御や実機ドライバは含まれていません

- 主に研究・開発用途での利用を想定しています

## Citation

```bibtex
@misc{agirobots_ros,
  title        = {AGIRobots ROS},
  author       = {{AGIRobots Inc.}},
  year         = {2026},
  howpublished = {https://github.com/AGIRobots/agirobots_ros}
}
```

## ライセンス（License）

TBD

