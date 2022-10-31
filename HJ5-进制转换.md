## 1. 题目描述

写出一个程序，接受一个十六进制的数，输出该数值的十进制表示。



示例：

```
输入：0xAA
输出：170
```



## 2. Solution

```python
while True:
    try:
        input = input()
        # int()函数，第一个参数为字符串，第二个参数为这个字符串是几进制的
        print(int(input, 16))
    except:
        break
    
```

