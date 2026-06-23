# vexiq-blocks-code

## English

This repository is a collection of code I wrote in VEX IQ Blocks.

The files are `.rbg` exports from block projects, sorted by competition flow, movement, navigation, and path scripting.

### How to use

1. Open VEXcode Blocks.
2. Import one `.rbg` file.
3. Match motors and sensor ports in the project.
4. Check distances, thresholds, and waits before running in match-like conditions.

### Detailed file catalog

#### competition
- `competition/complex-color-gate-task.rbg`  
  A multi-step competition path sequence with alternate forward turns and timed waits. It also sets different motor speeds for different parts, useful as a complex task skeleton.

#### motion
- `motion/motor-encoder-stop-after-distance.rbg`  
  Starts both motors and waits until right motor encoder reaches a target, then stops all motors. This is a distance-gated stop behavior.
- `motion/empty-template.rbg`  
  Empty template export with `task main()` only, used as a clean starting point for creating new Block programs.

#### navigation
- `navigation/distance-based-forward-reverse.rbg`  
  If front distance condition is within threshold, moves forward for one second; otherwise reverse for one second. Repeats forever. Useful for obstacle-aware reversal experiments.
- `navigation/line-follow-basic.rbg`  
  Simple grayscale-follow behavior with if/else: one motor stops while the other drives. This gives pivot-like correction on line boundaries.
- `navigation/encoder-turn-step.rbg`  
  Moves forward to one encoder threshold, performs a turn command, resets encoders, then continues. Useful for segmented path logic with movement checkpoints.

#### paths
- `paths/sequence-left-forward.rbg`  
  A repeated forward + turn chain, with multiple timing values. Suitable as a predefined path template.
- `paths/turn-forward-sequence-long.rbg`  
  Extended forward-turn chain variant for longer path sequencing.

### License

This repository is released under the MIT License. See [`LICENSE`](./LICENSE).

### Author note

All files in this repository are my own.

---

## 中文

这是我编写的 VEX IQ Blocks 程序合集，按任务和行为模块整理，便于复用。

### 使用方法

1. 打开 VEXcode Blocks。
2. 每次导入一个 `.rbg` 文件。
3. 匹配项目中的端口与电机。
4. 运行前先校准距离、阈值和等待时间。

### 文件详细说明

#### competition（比赛）
- `competition/complex-color-gate-task.rbg`  
  复杂动作链示例：包含前进、转向、不同电机速度和等待段，适合赛事流程拆解。

#### motion（运动）
- `motion/motor-encoder-stop-after-distance.rbg`  
  起步后依据右轮编码器达到指定距离停止。适合距离到达自动停车。
- `motion/empty-template.rbg`  
  空白模板，适合快速从块模式搭一个新任务。

#### navigation（导航）
- `navigation/distance-based-forward-reverse.rbg`  
  按距离阈值在前进和后退之间切换，循环执行，适合基础避障或边界反转。
- `navigation/line-follow-basic.rbg`  
  基础循线 if/else：一侧停转一侧前进进行修正。
- `navigation/encoder-turn-step.rbg`  
  编码器阈值 + 转向动作组成的分段导航。

#### paths（路径）
- `paths/sequence-left-forward.rbg`  
  预先定义的前进与左转连续链。
- `paths/turn-forward-sequence-long.rbg`  
  适合走更长路径的前进-转向组合版。

### 开源许可

本仓库使用 MIT 协议，详见 [`LICENSE`](./LICENSE)。

### 作者说明

本仓库文件全部由本人编写。
