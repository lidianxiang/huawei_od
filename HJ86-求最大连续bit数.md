## 1. 题目描述

求一个int类型数字对应的二进制数字中1的最大连续数，例如3的二进制为00000011，最大连续2个1

数据范围：数据组数：1\le t\le 5\1≤*t*≤5 ，1\le n\le 500000\1≤*n*≤500000 

进阶：时间复杂度：O(logn)\*O*(*l**o**g**n*) ，空间复杂度：O(1)\*O*(1) 



示例1:

```
输入：200
输出：2
说明：200的二进制表示是11001000，最多有2个连续的1。
```



## 2. Solution

```python
while True:
    try:
        x = int(input())
        byte_x = bin(x)[2:]
        # set去重，去掉分割出来的空值，然后按照长度进行降序排序
        lists = sorted(list(set(byte_x.split('0'))), key=lambda x:len(x),reverse=True)

        print(len(lists[0]))
            
    except:
        break
```

