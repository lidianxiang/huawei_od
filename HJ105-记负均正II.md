## 1.题目描述

输入 n 个整型数，统计其中的负数个数并求所有非负数的平均值，结果保留一位小数，如果没有非负数，则平均值为0

本题有多组输入数据，输入到文件末尾。

示例1:

```
输入：
    -13
    -4
    -7

输出：
    3
    0.0
```



## 2. Solution

```python
l1, l2 = [], []
while True:
    try:
        n = int(input())
        if n > 0:
            l1.append(n)
        if n < 0:
            l2.append(n)
    except:
        break
        
print(len(l2))
if sum(l1) == 0:
    print(0.0)
else:
    print(round(sum(l1)/len(l1), 1))
```

