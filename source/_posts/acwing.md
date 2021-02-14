---
title: acwing
date: 2021-02-10 17:32:44
tags: [技术分享]
---
# AcWing专栏
## 基础语法知识点
### 变量及输入输出
- 两个重要的头文件; iostream和cstdio; iostream - cin/cout | cstdio - scanf/printf;
- .h将所有的名字放在global namespace中，而新的方式（cstdio）是放在namespace std中。
- scanf/printf 效率比 cin/cout 高;
- %d %f %c %lf %lld;
- %05d - 前面补0/ %-05d 后面补0/ %5.1lf 前面补空(5代表最小宽度 可多不可少)
- ++a a++| c = a++; d = ++a;|d比c大;
### 判断
- && 的短路原则（前面不满足就不执行后面的）
- 