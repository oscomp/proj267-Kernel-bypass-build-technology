# proj267-Kernel-bypass-build-technology
## 标题

基于动态二进制翻译的内核旁路构建技术

## 项目描述

在内核设计中，用户程序通过标准的syscall接口调用内核组件，从而完成网络I/O等任务。然而，在用户态与内核态之间切换往往会带来大量性能开销。传统的旁路技术（如DPDK）尽管能够加速用户程序的网络I/O速度，但其提供了一套完全不同于标准syscall的接口，因此需要对已有程序做大量修改，开发难度大大增加。

本项目希望结合动态二进制翻译（Dynamic Binary Translation，DBT）技术，在运行过程中，动态地将一部分用户程序构建为在内核态执行（内核旁路），从而能减少用户态/内核态切换，加速网络I/O速度。该方法同时能够避免对用户代码进行修改，降低了开发难度。

## 预期目标

1. 对内核进行修改，建立实验性的内核旁路构建机制；
2. 针对常见的网络应用（如Socket通信），测试该机制所带来的性能提升；
3. 与现有的旁路技术（如DPDK、eBPF等）进行对比。

## 特征

- 从不同的维度（使用OS、扩展OS、实现OS、分析OS、硬件特征、应用需求….）设计操作系统相关的实验内容和比赛项目指导教程
- 文档、代码、问题、答疑交互过程都开放和开源的
- 支持各种硬件
    - 基于目前量产的处理器和开发板，比如：
        - D1哪吒开发板（基于平头哥C906 RV64 CPU）
        - K210开发板（基于K210处理器 RV64 CPU）
        - K510开发板（基于K510处理器 RV64 CPU）
        - StarFive开发板（基于U740 RV64 CPU）
        - SiFive Unmatch开发板（基于U740/U540 RV64 CPU）
        - 树莓派开发板（基于ARM处理器）

## 已有参考资料

- Zhou, Zhe, Yanxiang Bi, Junpeng Wan, Yangfan Zhou, and Zhou Li. “Userspace Bypass: Accelerating Syscall-Intensive Applications.” In 17th USENIX Symposium on Operating Systems Design and Implementation (OSDI 23), 33–49, 2023.

## 赛题分类

2.4.99 未归类运行时支撑

## 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生
- 允许学生参加大赛的多个不同题目，最终自己选择一个题目参与评奖
- 请遵循“2024全国大学生操作系统比赛”的章程和技术方案要求

## 难度

中等

## License

MIT License

## 所属赛道

2024全国大学生操作系统比赛的“OS功能挑战”赛道

## 项目导师

- 姓名：危荣广
- 单位：麒麟软件有限公司
- gitee ID：[https://gitee.com/wei90](https://gitee.com/wei90)
- email：[weirongguang@kylinos.cn](mailto:weirongguang@kylinos.cn)


- 姓名：陆云
- 单位：麒麟软件有限公司
- gitee ID：[https://gitee.com/luyun_kylin](https://gitee.com/luyun_kylin)
- email：[luyun@kylinos.cn](mailto:luyun@kylinos.cn)
