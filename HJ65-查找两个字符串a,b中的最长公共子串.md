## 1. 题目描述

查找两个字符串a,b中的最长公共子串。若有多个，输出在较短串中最先出现的那个。

注：子串的定义：将一个字符串删去前缀和后缀（也可以不删）形成的字符串。请和“子序列”的概念分开！

示例1:

```
输入：
    abcdefghijklmnop
    abcsafjklmnopqrstuvw

输出：jklmnop
```



## 2. Solution

```python
while True:
    try:
        a, b = input(), input()
        if len(a) > len(b):
            a, b = b, a 
        res = ''
        for i in range(0, len(a)):
            for j in range(i+1, len(a)):
                if a[i:j+1] in b and j-i+1 > len(res):
                    res = a[i:j+1]
        print(res)
    except:
        break
```

