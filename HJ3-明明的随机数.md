## 1. 题目描述

明明生成了N个1到500之间的随机整数，请你删去其中重复的数字，即相同的数字只保留一个，把其余相同的数去掉，然后再把这些数从小到大排序，按照排好的顺序输出。

输入描述：

第一行先输入随机整数的个数N。接下来的N行每行输入一个整数，代表明明生成的随机数。

示例：

```
输入：3
     2
     2
     1
输出：1
     2
说明：输入解释：第一个数字3，即这个小样例的个数为N=3，说明用计算机生成了3个1到500之间的随机整数，接下来每行一个随机数字，共3行，也即这3个随机数字为：2、2、1.
```



## 2. Solution

```python
while True:
    try:
        n = input()
        res = []
        for i in range(int(n)):
            res.append(int(input()))
            
        unique = list(set(res))
        unique.sort()
        for i in unique:
            print(i)
    except:
        break
```

