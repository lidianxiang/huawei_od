## 1. 题目描述

写出一个程序，接受一个由字符、数字和空格组成的字符串，和一个字符，然后输出输入字符串中该字符出现的次数。

示例：

```
输入：ABCabc
     A
输出：2
```



## 2. Solution

```python
import sys

str1 = input.lower()
str2 = input.lower()

print(str1.count(str2))
```

