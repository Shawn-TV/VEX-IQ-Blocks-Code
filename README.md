# VEX IQ Blocks Robot Routines

## English

This repository contains VEX IQ Blocks / graphical robot programs exported as `.rbg` files. The examples are organized by robot behavior: competition-style routines, encoder motion, sensor-based navigation, and preset path sequences.

Short description: VEX IQ Blocks robot routines for movement, line following, distance sensing, path sequences, and competition-style task flows.

## What is included

- `competition/` contains longer routines that combine several actions into one match-style flow.
- `motion/` contains small encoder or motor-distance examples.
- `navigation/` contains line-following, distance-triggered movement, and branch-based robot behavior.
- `paths/` contains preset route examples built from forward and turn steps.

## How to use these files

1. Download or clone this repository.
2. Open the VEX IQ Blocks / graphical programming environment that supports `.rbg` imports.
3. Import one `.rbg` file. Start with a small file such as `navigation/line-follow-basic.rbg` or `motion/motor-encoder-stop-after-distance.rbg`.
4. Open the robot configuration area before running the program. Check motor ports, sensor ports, and reversed motor directions against your real robot.
5. Place the robot on blocks or hold the drive wheels off the table for the first test.
6. Download the program to the VEX IQ Brain and run it slowly.
7. Tune speeds, wait times, encoder distances, and sensor thresholds for your chassis, floor color, and classroom field.

## Beginner notes

- `.rbg` files are exported graphical programs. They include block data plus generated RobotC-style source inside the file.
- Do not edit the XML by hand unless you are only making a very small configuration fix. It is safer to import the file, change the blocks, then export again.
- Distance and color values are not universal. A threshold that works on one floor or lighting setup may need to change on another field.
- If the robot drives backward or turns the wrong way, check the motor direction/reversed setting first.

## Program catalog

### competition

- `competition/complex-color-gate-task.rbg`
  - A longer competition-style sequence with forward movement, turns, speed changes, wait points, and color-sensor gates. It is useful for studying how a full routine can be built from smaller movement and sensor steps.

### motion

- `motion/motor-encoder-stop-after-distance.rbg`
  - Starts the drive motors, watches the right motor encoder, and stops all motors after the target distance is reached. This is a good first example for learning encoder-based stopping.

### navigation

- `navigation/distance-based-forward-reverse.rbg`
  - Uses two distance sensors to choose between forward and reverse movement. This is useful for obstacle or gate-style demonstrations where the robot reacts to objects in front of or behind it.
- `navigation/encoder-turn-step.rbg`
  - Drives forward to an encoder count, turns, resets the encoders, then drives another segment. Use this as a template for step-by-step autonomous paths.
- `navigation/line-follow-basic.rbg`
  - A simple grayscale line follower. One side of the drivetrain pauses while the other side moves, so the robot nudges itself back toward the line.

### paths

- `paths/sequence-left-forward.rbg`
  - A short route made from repeated forward movement and left turns. It is best for testing a simple square-like path pattern.
- `paths/turn-forward-sequence-long.rbg`
  - A longer path routine with more forward segments and turn corrections. Use it when you want a bigger autonomous path example to modify.

## License

This repository is released under the MIT License. See [`LICENSE`](./LICENSE).

## 中文

这个仓库存放的是 VEX IQ Blocks / 图形化机器人程序，文件格式是 `.rbg`。这些程序按机器人行为分类，包括竞赛风格流程、编码器运动、传感器导航和预设路线。

短描述：VEX IQ Blocks 机器人例程，覆盖移动、循线、距离传感、路径序列和竞赛风格任务流程。

## 仓库里有什么

- `competition/`：更长的动作链，适合看完整竞赛流程怎么拼起来。
- `motion/`：较小的电机和编码器距离示例。
- `navigation/`：循线、距离触发、条件分支等导航行为。
- `paths/`：由前进和转向组成的固定路线。

## 如何使用这些文件

1. 下载或克隆这个仓库。
2. 打开支持 `.rbg` 导入的 VEX IQ Blocks / 图形化编程环境。
3. 导入一个 `.rbg` 文件。新手建议先看 `navigation/line-follow-basic.rbg` 或 `motion/motor-encoder-stop-after-distance.rbg`。
4. 运行前先检查机器人配置：电机端口、传感器端口、电机是否反向，都要和真实机器人一致。
5. 第一次测试时，把机器人架起来，或者让驱动轮离开桌面。
6. 下载到 VEX IQ Brain 后低风险运行。
7. 根据你的底盘、地面颜色、场地和光线，调整速度、等待时间、编码器距离和传感器阈值。

## 新手注意

- `.rbg` 是图形化程序导出文件，里面包含积木数据，也包含生成出来的 RobotC 风格源码。
- 不建议手写修改 XML。更稳的方式是导入文件、在图形界面里改积木、再重新导出。
- 距离和颜色阈值不是固定答案。换地面、换光线、换机器人都可能要重新调。
- 如果机器人方向反了，先检查电机端口和反向设置。

## 程序目录

### competition

- `competition/complex-color-gate-task.rbg`
  - 较长的竞赛风格动作链，包含前进、转向、速度变化、等待点和颜色传感器判断。适合学习完整自动流程如何由小动作组合出来。

### motion

- `motion/motor-encoder-stop-after-distance.rbg`
  - 启动驱动电机，读取右侧电机编码器，到达目标距离后停止所有电机。适合作为编码器停止的入门例子。

### navigation

- `navigation/distance-based-forward-reverse.rbg`
  - 使用两个距离传感器在前进和后退之间切换。适合障碍物、闸门或距离反应类演示。
- `navigation/encoder-turn-step.rbg`
  - 先按编码器距离前进，再转向、重置编码器，然后继续下一段。适合作为分段自动路线模板。
- `navigation/line-follow-basic.rbg`
  - 基础灰度循线。通过让一侧电机停、一侧电机动，把机器人轻微拉回线附近。

### paths

- `paths/sequence-left-forward.rbg`
  - 由前进和左转组成的短路径，适合测试类似方形路线的基础路径。
- `paths/turn-forward-sequence-long.rbg`
  - 更长的路径例程，包含更多前进段和转向修正。适合在更大场地上改成自己的自动路径。

## 开源许可

本仓库使用 MIT 协议，详见 [`LICENSE`](./LICENSE)。
