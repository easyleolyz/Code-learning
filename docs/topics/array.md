# 数组专题（Array）

> 记录与数组相关的知识点和典型题目，来源包括：左程云课程、代码随想录、LeetCode、牛客网等。

## 1. 知识点概览

- 数组的基础性质（连续内存、下标访问 O(1)）
- 常见操作：遍历、双指针、滑动窗口、前缀和等
- 与其他结构的联动：数组 + 哈希表、数组 + 栈 等

## 2. 典型题目列表

| 序号 | 题目 | 平台 | 难度 | 代码路径 | 来源 | 技巧标签 |
| ---- | ---- | ---- | ---- | -------- | ---- | -------- |
| 1    | Two Sum（两数之和） | LeetCode 1 | Easy | `problems/leetcode/python/LC0001_two_sum.py` | 左程云-入门 / 代码随想录 | 哈希表 |
| 2    | Contains Duplicate | LeetCode 217 | Easy | `problems/leetcode/python/LC0217_contains_duplicate.py` | 代码随想录-数组篇 | 哈希表 |
| ...  |                      |             |      |                                        |                  |        |

## 3. 题解示例：LeetCode 1. Two Sum

### 题目大意

给定一个整数数组 nums 和一个目标值 target，在数组中找出两个数，使得它们的和等于 target，返回这两个数的下标（下标从 0 开始）。假设每种输入只会对应一个答案，同一个元素不能使用两次。

### 解题思路

**思路 1：暴力枚举(O(n^2))**

- 双重循环，枚举所有二元组 (i, j)，检查 `nums[i] + nums[j] == target`。
- 简单但效率不高。

**思路 2：哈希表（O(n)）**

- 用字典 / HashMap 记录“值 → 下标”。
- 遍历数组，对当前值 `x = nums[i]`，查哈希表中是否存在 `target - x`：
  - 若存在，说明找到了这两个数，返回对应下标；
  - 若不存在，把当前值和下标存入哈希表继续向后。

### Python 代码

```python
from typing import List

class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        index = {}
        for i, x in enumerate(nums):
            y = target - x
            if y in index:
                return [index[y], i]
            index[x] = i
        return []
```

### Java 代码
```Java
import java.util.HashMap;
import java.util.Map;

class Solution {
    public int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> index = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int x = nums[i];
            int y = target - x;
            if (index.containsKey(y)) {
                return new int[]{index.get(y), i};
            }
            index.put(x, i);
        }
        return new int[0];
    }
}

```

### 复杂度分析
- 时间复杂度：O(n)，每个元素最多访问两次（查找 + 插入哈希表）。

- 空间复杂度：O(n)，哈希表在最坏情况下存储 n 个元素。

### 易错点 / 备注
- 注意不要把当前值先放进哈希表再查，否则会把自己和自己匹配上
- 若题目要求返回的是值（而不是下标），则稍微调整返回内容即可