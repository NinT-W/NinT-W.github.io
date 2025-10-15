---
title: DFS Practice
published: 2025-10-14
description: 'DFS—深度优先搜索算法题目汇总'
image: ''
tags: [DFS,剪枝]
category: 'Algorithm'
draft: false 
lang: ''
---

## [P4397 [JLOI2014] 聪明的燕姿](https://www.luogu.com.cn/problem/P4397)

#### 简化题意

给出正整数 $S$，找到所有满足正约数和等于 $S$ 的数字

#### 解题思路

**_约数和定理_** 对于正整数 $X$，易得 $ X = \prod_{i=1}^{k}{{P_i}^{a_i}}$， $X$ 的约数和 $S = \prod_{i=1}^{k}\sum_{j=0}^{a_i}{{P_i}^j}$

因此，只需枚举 $S$ 以内的质数与其指数，根据约数和定理与 $S$ 进行比较，即可找到答案

#### 优化策略 [Code](https://github.com/NinT-W/Algorithm-Practice/blob/main/LuoGu/P4397.cpp)

首先，直接采用枚举的策略显然不现实，因此考虑使用DFS优化筛选质数与其指数，参数 $step, num, now$ 分别表示剩余质数编号的最小值，约数和的剩余部分，已选质数构成的值，显然当 $num = 1$ 时，$now$ 即为答案之一

此外，由于 $S$ 的数据范围较大，无法用线性筛预处理出范围内的所有质数，需要考虑约数和定理的性质

显然，若 $X$ 的一个质约数 $P_i > \sqrt{S}$，则其指数 $a_i \leqslant{1}$，否则 $\sum_{j=0}^{a_i}{{P_i}^j} > S$，且这样的质约数只会有一个，并是 $X$ 的最大质约数，只需在每步搜索时判断参数 $$num-1$$ 是否为质数即可筛选出，时间复杂度为 $O(\sqrt{P_i})$ ; 而对于小于等于 $\sqrt{S}$ 的质数，通过线性筛即可进行预处理，时间复杂度为 $O(\sqrt{S})$
