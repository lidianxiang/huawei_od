## 1. 题目描述

+ 输入一个字符串，请按长度为8拆分每个输入字符串并进行输出；
+ 长度不是8整数倍的字符串，请在后面补数字0，空字符串不处理

输入描述：连续输入字符串（每个字符串长度小于等于100）

输出描述：依次输出所有分割后的长度为8的新字符串



示例：

```
输入：abc
输出：abc00000
```



## 2. Solution

```python
while True:
    try:
        strs = input()
        length = len(strs)

        for i in range(0, length, 8):
            # print("{0:0<8s}".format(strs[i:i+8]))
            # format中的`<`表示左对齐，`:0`表示不足以0作为填充，数字8表示最长长度为8
            print("{:0<8}".format(strs[i:i+8]))
    except:
        break
```

