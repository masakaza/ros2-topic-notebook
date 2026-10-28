# ROS 2 话题通信学习手册

面向初学者的 ROS 2 Topic 通信实践项目，围绕 [ROS2 理论与实践课程](https://rzl6.github.io/ROS2_Tuition/) 第 2 章 2.2「话题通信」的学习方向，结合 ROS 2 Humble 官方教程补充概念、命令与调试方法。这里的示例代码为教学用途重新编写，并非原课程代码的逐字复制。

## 环境

- Ubuntu 22.04 + ROS 2 Humble
- C++ / `ament_cmake`
- `rclcpp`、`std_msgs`

## 快速开始

```bash
# 加载 ROS 2 环境
source /opt/ros/humble/setup.bash

# 创建工作空间
mkdir -p ~/ros2_ws/src
```

将本仓库中的 `src/topic_demo_cpp` 复制到 `~/ros2_ws/src/topic_demo_cpp`，然后：

```bash
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src -r -y --rosdistro humble
colcon build --packages-select topic_demo_cpp
source install/setup.bash
```

分别在两个终端运行（每个终端都要 source 环境）：

```bash
ros2 run topic_demo_cpp talker
ros2 run topic_demo_cpp listener
```

talker 每秒向 `/chatter` 发布一条字符串消息，listener 收到后打印。使用 `Ctrl+C` 停止。

## 目录

```text
docs/                         # 8 篇分主题说明文档
src/topic_demo_cpp/           # 可编译的 C++ 发布者/订阅者功能包
scripts/setup_workspace.sh    # 可选的工作空间复制与编译辅助脚本
README.md                     # 项目入口
SOURCE_INDEX.md               # 代码与文档索引
CONTRIBUTING.md               # 维护和协作说明
LICENSE
.gitignore
```

## 学习路线

1. [ROS 2 话题通信基础](docs/01-ros2-basics.md)
2. [工作空间与功能包](docs/02-workspace-and-package.md)
3. [编译、加载与运行](docs/03-build-and-run.md)
4. [话题命令行工具](docs/04-topic-cli.md)
5. [C++ 代码逐段解读](docs/05-code-walkthrough.md)
6. [QoS 与话题命名](docs/06-qos-and-naming.md)
7. [常见问题排查](docs/07-troubleshooting.md)
8. [动手练习](docs/08-exercises.md)

## 参考资料

- [ROS2 理论与实践课程](https://rzl6.github.io/ROS2_Tuition/)
- [ROS 2 Humble 文档](https://docs.ros.org/en/humble/)
- [官方 C++ 发布者与订阅者教程](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Writing-A-Simple-Cpp-Publisher-And-Subscriber.html)
- [官方 Topic 概念说明](https://docs.ros.org/en/humble/Concepts/Basic/About-Topics.html)

本仓库是独立的学习笔记项目，与课程作者及 ROS 2 官方无隶属关系。许可信息见 `LICENSE`。
