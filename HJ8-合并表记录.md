## 1. 题目描述

数据表记录包含表索引index和数值value，请对表索引相同的记录进行合并，即将相同索引的数值进行求和运算，输出按照index值升序进行输出。



示例1:

```
输入:
    s4
    0 1
    0 2
    1 2
    3 4

输出：
    0 3
    1 2
    3 4
```



## 2. Solution

```python
n = int(input())
dic = {}

for i in range(n):
    line = input().split(' ')
    key, value = int(line[0]), int(line[1])
    dic[key] = dic.get(key, 0) + value
    
for each in sorted(dic):
    print(each, dic[each])
```

