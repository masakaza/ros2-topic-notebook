# 源码与文档索引

## ROS 2 C++ 功能包

- `src/topic_demo_cpp/src/talker.cpp`：定时发布 `std_msgs/msg/String` 的节点。
- `src/topic_demo_cpp/src/listener.cpp`：订阅 `/chatter` 并打印消息的节点。
- `src/topic_demo_cpp/CMakeLists.txt`：定义依赖、两个可执行目标和安装规则。
- `src/topic_demo_cpp/package.xml`：功能包元数据与依赖声明。

## 文档

- `docs/01-ros2-basics.md`：节点、话题、消息、Topic/Service/Action 区别。
- `docs/02-workspace-and-package.md`：工作空间与创建功能包。
- `docs/03-build-and-run.md`：rosdep、colcon、source、ros2 run。
- `docs/04-topic-cli.md`：topic list/info/echo/hz/pub、node 命令。
- `docs/05-code-walkthrough.md`：发布订阅 C++ 代码解释。
- `docs/06-qos-and-naming.md`：QoS、相对/绝对名称和 remapping。
- `docs/07-troubleshooting.md`：常见错误排查。
- `docs/08-exercises.md`：动手练习与自测。
