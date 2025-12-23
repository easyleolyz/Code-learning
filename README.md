# Code-learning

> 基于 **左程云 B站算法课（入门 → 必备 → 扩展 → 挺难）** + **代码随想录题单** + **LeetCode / 牛客网** 的个人算法与代码能力提升仓库。

## 仓库目标

- 系统复习与巩固数据结构与算法，服务于：
  - 互联网大厂手撕代码 / 笔试 / 面试（字节、腾讯等）
  - 考研复试机试（北大软微、浙大软院、上交计院等）
- 以 **Python / Java** 为主，逐步积累可复用的算法模板和代码风格。
- 将刷题过程整理为 **文档 + 题解 + 题单索引**，形成结构清晰、可扩展的个人知识库。

## 学习来源

- B 站：左程云个人账号
  - 入门篇 → 必备篇 → 扩展篇 → 挺难篇
  - 本仓库在 `docs/sources/zcy/` 下对课程内容和例题进行归纳整理。
- 题单：代码随想录（程序员 Carl）
  - 在 `docs/sources/codetop/` 维护对应题单与进度。
- 在线 OJ 平台：
  - LeetCode / 力扣（主力）
  - 牛客网（剑指 Offer、企业真题、机试题）

> 本仓库仅保存本人整理的笔记与代码，不包含任何课程视频或付费资料的原始内容。

## 目录结构

```text
Code-learning/
├─ README.md                 # 仓库说明
├─ docs/                     # 文档（笔记 + 题解 + 计划）
│  ├─ sources/               # 按学习“来源”整理
│  │  ├─ zcy/                # 左程云 B站课程相关
│  │  │  ├─ zcy_intro.md     # 入门篇：知识点 + 例题索引
│  │  │  ├─ zcy_must.md      # 必备篇：知识点 + 例题索引
│  │  │  ├─ zcy_extend.md    # 扩展篇：知识点 + 例题索引
│  │  │  └─ zcy_hard.md      # 挺难篇：知识点 + 例题索引
│  │  └─ codetop/            # 代码随想录题单
│  │     ├─ codetop_intro.md # 路线说明
│  │     └─ codetop_list.md  # 题单索引与进度
│  ├─ topics/                # 按“算法专题”整理的总结
│  │  ├─ array.md
│  │  ├─ linked-list.md
│  │  ├─ stack-queue.md
│  │  ├─ tree.md
│  │  ├─ graph.md
│  │  ├─ dp.md
│  │  └─ others.md
│  └─ roadmap/               # 学习规划 / 阶段性总结
│     └─ roadmap_2025.md
├─ problems/                 # 具体题目代码（按平台 + 语言）
│  ├─ leetcode/
│  │  ├─ python/
│  │  │  └─ LC0001_two_sum.py
│  │  └─ java/
│  │     └─ LC0001_TwoSum.java
│  └─ niuke/
│     ├─ python/
│     └─ java/
├─ templates/                # 常用模板（DFS/BFS/DP/并查集等）
│  ├─ python/
│  └─ java/
├─ .vscode/                  # VSCode 配置（WSL 环境下开发）
│  └─ settings.json
└─ .gitignore                # Git 忽略规则


```

## 命名与标签约定

### 1.代码文件

- LeetCode:
  - 文件名：LC{四位题号}_{简短英文题名}.{py/java}
  - LC0001_two_sum.py

- 牛客网:
  - 文件名:NK_{板块/标签}_{简短中文题名}.{py/java}
  - NK_剑指Offer_反转链表.py

### 2.文件内注释

- 来源: 左程云-必备篇 / 左程云-扩展篇 / 代码随想录-数组篇 / ...
- 平台: LeetCode / 牛客网
- 题目: xxx（可附链接）
- 标签: array, dp, linked-list, easy/mid/hard 等

## 学习与刷题流程

### 1.看课 / 读题单

    左程云：按「入门 → 必备 → 扩展 → 挺难」顺序学习；

    代码随想录：按题单模块（数组、链表、树、DP 等）推进。

### 2.在OJ上做题

    先在平台上 AC

    再将代码整理到本仓库的 problems/ 下


### 3.写文档 / 题解

    在 docs/sources/ 中记录“来源 → 涉及哪些题目 → 对应代码文件”；

    在 docs/topics/ 中对某一类专题做更系统的总结。

### 4.提交Github
    
    小步提交（每完成若干题 / 一个小模块就 commit 一次），保留清晰的成长轨迹。


## 环境说明

    本地开发环境：

    Windows + WSL2 (Ubuntu 等)

    VSCode（通过 Remote - WSL 插件打开本仓库）

    语言：

    Python 3.x

    Java 8+



## 进度记录
    |---|---|
    |时间|	内容
    |2025-寒假	| 左程云-入门 + 必备，LeetCode 数组/链表，高频简单题
    |2025-春季	|左程云-扩展 + 挺难，动态规划/树/图，开始真题模拟