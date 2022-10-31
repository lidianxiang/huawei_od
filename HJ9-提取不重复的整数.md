## 1. 题目描述

输入一个int型整数，按照从右往左的阅读顺序，返回一个不含重复数字的新的整数，保证输入的整数最后一位不是0.



示例1:

```
输入：9876673
输出：37689
```



## 2. Solution

```python
num = str(input())[::-1]

res = []

for ch in num:
    if ch not in res:
        res.append(ch)
print("".join(res))
```

