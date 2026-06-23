# vexiq-blocks-code

## English

This repository is a collection of code I wrote in VEX IQ Blocks.

It contains reusable logic blocks for navigation, motion, path scripting, and competition tasks.

### How to use

1. Open the VEX IQ Blocks or VEXcode Blocks workspace.
2. Import one `.rbg` file at a time.
3. Configure motors and sensor ports in the block project to match your robot.
4. Calibrate timing and threshold constants after importing.

### How these files are organized

#### competition
- `competition/complex-color-gate-task.rbg`  
  Multi-step color-gate style competition routine.

#### motion
- `motion/motor-encoder-stop-after-distance.rbg`  
  Encoder distance stop behavior.
- `motion/empty-template.rbg`  
  Empty template for building new block routines.

#### navigation
- `navigation/distance-based-forward-reverse.rbg`  
  Distance-based forward and reverse flow.
- `navigation/line-follow-basic.rbg`  
  Basic line following logic.
- `navigation/encoder-turn-step.rbg`  
  Encoder-based turn-and-step sequence.

#### paths
- `paths/sequence-left-forward.rbg`  
  Left turn then forward sequence demonstration.
- `paths/turn-forward-sequence-long.rbg`  
  Extended turn-forward chaining routine.

### License

This repository is released under the MIT License. See [`LICENSE`](./LICENSE).

### Author note

All files in this repository are my own.

---

## 中文

这是我编写的 VEX IQ Blocks 程序合集，按模块整理，可复用用于行为逻辑与任务流程搭建。

内容覆盖导航、运动、路径序列和比赛任务模块，适合做课程复盘和动作复用。

### 使用方法

1. 打开 VEX IQ Blocks / VEXcode Blocks。
2. 每次导入一个 `.rbg` 文件。
3. 在项目里按实际接线调整电机和传感器端口。
4. 运行前先做阈值与时间参数标定。

### 文件归类与作用

#### competition（比赛）
- `competition/complex-color-gate-task.rbg`  
  复杂双色门任务风格的流程示例。

#### motion（运动）
- `motion/motor-encoder-stop-after-distance.rbg`  
  编码器距离到达后的停机动作。
- `motion/empty-template.rbg`  
  空白模板，用于快速搭建新流程。

#### navigation（导航）
- `navigation/distance-based-forward-reverse.rbg`  
  按距离切换前进/后退的流程。
- `navigation/line-follow-basic.rbg`  
  基础循线逻辑。
- `navigation/encoder-turn-step.rbg`  
  编码器驱动的转向与分步动作。

#### paths（路径）
- `paths/sequence-left-forward.rbg`  
  左转后前进序列示例。
- `paths/turn-forward-sequence-long.rbg`  
  长序列转向前进流程。

### 开源许可

仓库使用 MIT 协议，详见 [`LICENSE`](./LICENSE)。

### 作者说明

本仓库文件全部由本人编写。
