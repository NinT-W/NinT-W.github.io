---
title: Computer Systems & Architecture
published: 2025-10-17
description: 'University of Leeds: Computer System & Architecture'
image: ''
tags: []
category: 'Concept'
draft: false 
lang: ''
---

# 0x01 System Architecture & History

#### Computer Architecture & Organisation

Architecture: As the **logical design** of the computer, defining the **programmer-visible attributes** of a system, all of which have a direct impact on the **logical execution** of a program.

Organisation: As the **physical** **implementation** (物理实现) of the architecture, defining **how** components are built, arranged and connected using electronics.

Same basic architecture gives code (机器编码) compatibility (至少是向后兼容), but the organisation differs between different versions.

#### Computer Structure

Structure is the way of components related to each other, and function is the operation of individual components.

##### Basic Functions

- **Data Processing 数据处理** 计算 / 转换 / 分析
- **Data Storage 数据存储** Long-term / Short-term
- **Data Movement 数据移动** I/O 输入输出 Data Communications 数据通信
- **Control 控制** 根据指令统筹协调各功能部件

##### Computer Components

- **CPU 中央处理器** 控制硬件操作 解释并执行来自硬件和软件的指令
- **Main Memory 主存储器** 即内存 存储数据和程序指令
- **Input/Output 输入输出** 实现数据与输入输出信号的转换
- **System Bus 系统总线** 在CPU/内存/输入输出设备之间传输数据的公共通道
- **Co-processors 协处理器** 例如GPU (图形) Crypto-processor (加密)

##### CPU Components

- **Control Unit 控制单元** 控制CPU的运行从而控制电脑
- **Arithmetic and Logic Unit 算术逻辑单元** ALU 进行Data Processing
- **Registers 寄存器** 存放CPU正在处理的数据和指令
- **CPU Interconnection CPU互连** 实现上述三个原件的通信
