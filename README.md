# vexiq-blocks-code

## English

This repository stores VEX IQ Blocks exports (`.rbg`) converted to practical behavior modules.

## What’s inside

- `competition/` for competition-style task chains.
- `motion/` for distance/encoder style movement.
- `navigation/` for follow, reverse, and branching movement.
- `paths/` for predefined path scripts.

## How to use

1. Open VEXcode Blocks.
2. Import one `.rbg` file.
3. Check robot configuration in the embedded `<RobotConfiguration>` section and update ports if needed.
4. Adjust speed, wait, and threshold constants before classroom demo or match test.

## Detailed catalog (English)

### competition
- `competition/complex-color-gate-task.rbg` — Complex sequence export with mixed turning, forward movement, motor speed overrides, wait points, and color-sensor loops, including a repeat-until timeout block at the end.

### motion
- `motion/motor-encoder-stop-after-distance.rbg` — Starts two motors and waits until the right motor encoder reaches the target distance, then calls `stopAllMotors()`.

### navigation
- `navigation/distance-based-forward-reverse.rbg` — Repeats forever; drives forward at distance threshold, otherwise runs reverse branch using two distance sensors and one-second timed moves.
- `navigation/encoder-turn-step.rbg` — Drives forward to encoder count, performs a left turn, resets encoders, then drives again.
- `navigation/line-follow-basic.rbg` — Basic `if/else` line follow on grayscale: one side motor pauses while the other runs.

### paths
- `paths/sequence-left-forward.rbg` — Repeated forward + left-turn chain useful as a short predefined route pattern.
- `paths/turn-forward-sequence-long.rbg` — Extended sequence for long paths with more forward segments, multiple left turns, and recovery right turns.

## Format notes

Each `.rbg` contains both Blocks XML-like commands and embedded generated RobotC source inside a `<CSource>` block. Port names and speeds should be tuned for your robot.

## License

This repository is released under the MIT License. See [`LICENSE`](./LICENSE).

## 中文

这是我自己的 VEX IQ Blocks 程序合集，按模块分类，便于复用和对照修改。

## 使用方式

1. 打开 VEXcode Blocks。
2. 导入 `.rbg` 文件。
3. 检查内嵌 `<RobotConfiguration>` 的端口映射并按你的机器人调整。
4. 调整速度、等待时间和阈值后再上机测试。

## 详细目录（中文）

### 赛事（competition）
- `competition/complex-color-gate-task.rbg` — 赛事风格复杂流程，包含转向、时序、速度控制和颜色传感器等待条件。

### 运动（motion）
- `motion/motor-encoder-stop-after-distance.rbg` — 两侧驱动启动，达到编码器阈值后停止。

### 导航（navigation）
- `navigation/distance-based-forward-reverse.rbg` — 距离阈值触发的前进与后退切换。
- `navigation/encoder-turn-step.rbg` — 编码器分段行驶+转向+重置。
- `navigation/line-follow-basic.rbg` — 灰度阈值简单循线。

### 路径（paths）
- `paths/sequence-left-forward.rbg` — 短路径演示的左转前进行组。
- `paths/turn-forward-sequence-long.rbg` — 更长路径版本，适合大场景演示。

## 开源许可

本仓库使用 MIT 协议，详见 [`LICENSE`](./LICENSE)。
