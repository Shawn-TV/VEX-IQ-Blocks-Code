# VEX-IQ-Blocks-Code

## English

This repository stores VEX IQ Blocks / graphical programming exports that I wrote while working on VEX IQ movement, sensors, and simple autonomous routines.

These files are for VEX IQ robots. They use a VEX IQ Brain, VEX IQ smart motors, and different VEX IQ sensors depending on the file, such as color, distance, touch/bumper, gyro, and Touch LED sensors.

## Quick start

1. Download this repository or open the file you want to use from GitHub.
2. Open the VEX IQ Blocks / graphical programming software that can import `.rbg` files.
3. Import one `.rbg` file. Start with a small one before trying the longer competition file.
4. Check the robot configuration after importing. The motor ports and sensor ports in the file must match your real robot.
5. Put the robot on blocks or lift the wheels for the first test.
6. Download the program to the VEX IQ Brain.
7. Change speeds, wait times, encoder distances, and sensor thresholds until it fits your own robot.

## What the folders mean

- `competition/` has a longer mixed routine.
- `motion/` has a small encoder-based movement example.
- `navigation/` has line following, distance sensing, and step movement examples.
- `paths/` has fixed path sequences made from forward and turn blocks.

## Programs

### `competition/complex-color-gate-task.rbg`

This is the longest Blocks program in the repository. It mixes turns, forward movement, motor speed changes, short waits, and several color-sensor checks.

The routine starts with movement steps, then uses the color sensor to wait for grayscale values before moving an arm or mechanism motor. Near the end it uses a timed repeat-until section, where the robot checks the color sensor and makes small left/right corrections.

Use this as a reference for a more complete autonomous task flow. Before running it, check all motor and sensor ports carefully, especially the drive motors, color sensor, arm motor, and any sensor used for timing or stopping.

### `motion/motor-encoder-stop-after-distance.rbg`

This is a simple encoder-distance example. It starts the left and right drive motors, watches the right motor encoder, and stops all motors after the encoder reaches the target value.

This is useful when you want the robot to drive roughly a fixed distance instead of only using a timed delay. The target encoder value and motor speeds should be adjusted for your own wheel size and robot speed.

### `navigation/distance-based-forward-reverse.rbg`

This program uses two distance sensors. In a forever loop, it checks one distance sensor and drives forward when the object is close enough, then checks another distance sensor and drives backward when that side is close enough.

It is mainly a sensor reaction example. It is useful for testing how a robot can respond to objects in front of or behind it. Make sure the two distance sensors are actually plugged into the ports shown in the robot configuration.

### `navigation/encoder-turn-step.rbg`

This is a step-by-step movement routine. The robot drives until the left motor reaches an encoder value, turns left, resets the motor encoders, and then drives another encoder-based segment.

Use this as a starting point for making a simple autonomous path. If the robot turns too much or not enough, change the turn amount or the encoder target values.

### `navigation/line-follow-basic.rbg`

This is a basic line follower using a grayscale/color sensor threshold. If the grayscale value is above the threshold, one side of the drivetrain moves and the other side stops. If the value is below the threshold, the sides switch.

This makes the robot wiggle along an edge between light and dark. You will probably need to change the threshold value for your own field, tape, lighting, and sensor height.

### `paths/sequence-left-forward.rbg`

This is a fixed path made from repeated forward moves and left turns. It does not use sensors to correct itself; it just follows the saved movement sequence.

It is useful for testing a basic square-like or route-like path. If the robot drifts, adjust the forward distances and turn amounts.

### `paths/turn-forward-sequence-long.rbg`

This is a longer fixed path sequence. It has several forward moves, multiple left turns, and a couple right turns near the end.

Use this when you want to study a longer autonomous path made only from movement blocks. Since it is not sensor-corrected, the result depends a lot on battery level, surface, wheel grip, and turn calibration.

## Notes

- `.rbg` files are exported graphical programs. They also contain generated RobotC-style source inside the file.
- It is better to import and edit them in the Blocks software instead of editing the file text by hand.
- Sensor thresholds are not universal. Re-test them whenever the room lighting or field surface changes.

## License

This repository uses the MIT License. See [`LICENSE`](./LICENSE).

## 中文

这个仓库存的是我自己写的 VEX IQ Blocks / 图形化程序导出文件，主要是 VEX IQ 的移动、传感器和简单自动流程。

这些文件是给 VEX IQ 机器人用的。一般会用到 VEX IQ Brain、VEX IQ 智能电机，还有不同的 VEX IQ 传感器，比如颜色传感器、距离传感器、触碰/bumper、陀螺仪、Touch LED 等。

## 快速开始

1. 下载这个仓库，或者从 GitHub 打开你想用的文件。
2. 打开可以导入 `.rbg` 的 VEX IQ Blocks / 图形化编程软件。
3. 导入一个 `.rbg` 文件。建议先从短的程序开始，不要一上来就跑最长的比赛流程。
4. 导入后先检查机器人配置。文件里的电机端口和传感器端口必须和你的真实机器人一致。
5. 第一次测试时，把机器人架起来，或者让轮子离开桌面。
6. 下载到 VEX IQ Brain 后再运行。
7. 根据自己的机器人修改速度、等待时间、编码器距离和传感器阈值。

## 文件夹说明

- `competition/`：比较长的混合流程。
- `motion/`：编码器运动小例子。
- `navigation/`：循线、距离传感、分步运动。
- `paths/`：由前进和转向组成的固定路线。

## 程序说明

### `competition/complex-color-gate-task.rbg`

这是仓库里最长的 Blocks 程序。它把转向、前进、电机速度调整、短等待、颜色传感器判断放在一个流程里。

程序前面是移动步骤，后面多次等待颜色传感器的灰度值达到条件，再控制一个手臂或机构电机。结尾还有一个带时间限制的重复判断，会根据颜色传感器做左右小修正。

这个文件适合用来看一个比较完整的自动任务流程是怎么拼起来的。运行前一定要检查端口，尤其是左右驱动电机、颜色传感器、机构电机和用于停止/判断的传感器。

### `motion/motor-encoder-stop-after-distance.rbg`

这是一个简单的编码器距离示例。程序会启动左右驱动电机，读取右侧电机编码器，到达目标值后停止所有电机。

如果你不想只靠延时控制距离，可以参考这个文件。编码器目标值和电机速度需要根据自己的轮子大小、机器人重量和速度来改。

### `navigation/distance-based-forward-reverse.rbg`

这个程序用两个距离传感器。在无限循环里，它先检查一个距离传感器，满足条件就前进；再检查另一个距离传感器，满足条件就后退。

它主要是一个传感器反应例子，适合测试机器人根据前后物体距离做动作。使用前要确认两个距离传感器插在配置里的端口上。

### `navigation/encoder-turn-step.rbg`

这是一个分步骤移动程序。机器人先走到左电机编码器目标值，然后左转，接着重置编码器，再走下一段编码器距离。

这个文件适合当作简单自动路线的起点。如果转得太多或太少，就改转向量；如果前进距离不对，就改编码器目标值。

### `navigation/line-follow-basic.rbg`

这是一个基础循线程序，用颜色/灰度传感器的阈值判断当前在深色还是浅色区域。高于阈值时一侧电机走、另一侧停；低于阈值时反过来。

这样机器人会沿着深浅交界线左右修正前进。不同场地、胶带、光线、传感器高度都会影响阈值，所以大概率要重新调。

### `paths/sequence-left-forward.rbg`

这是一个固定路线程序，由多次前进和左转组成。它不靠传感器修正，只按保存好的动作顺序走。

适合测试类似方形路线或短路径路线。如果机器人越走越偏，就调前进距离和转向角度。

### `paths/turn-forward-sequence-long.rbg`

这是一个更长的固定路线。里面有多段前进、多次左转，最后还有右转修正。

它适合用来看比较长的自动路径怎么写。因为没有传感器纠偏，效果会受电池电量、地面、轮胎摩擦和转向校准影响。

## 注意

- `.rbg` 是图形化程序导出文件，里面也包含生成出来的 RobotC 风格源码。
- 最好导入到 Blocks 软件里改，不建议直接手写改文件内容。
- 传感器阈值不是固定答案。换光线、换地面、换机器人都要重新测。

## 开源许可

本仓库使用 MIT 协议，详见 [`LICENSE`](./LICENSE)。
