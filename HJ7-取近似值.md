## 1. 题目描述

接受一个正浮点数，输出该数值的近似整数值，如果小数点后数值大于等于0.5，向上取整；小于0.5则向下取整。

示例1:

```
输入：5.4
输出：6
```

示例2:

```
输入：5.4
输出：5
```



## 2. Solution

```python
n = float(input())
y = lambda x: int(x+0.5)
print(y(n))
```



## 3. Solution2

```python
def func(n):
    a = int(n+0.5)
    return a

b = float(input())
print(func(b))
```

