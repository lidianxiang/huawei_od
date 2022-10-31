## 1. 题目描述

输入一个int型正整数，计算出该int型数据在内存中存储1的个数

示例1:

```
输入：5
输出：2
```



## 2. Solution

```python
n = int(input())
print(bin(n).count('1'))
```

